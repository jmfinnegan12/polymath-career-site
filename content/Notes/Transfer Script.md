
# Website Content Transfer Script
This script "robust copies" all content from `obsidianRoot` to `gitRoot`. 

Robust copy is a computationally efficient way to mirror contents of one folder to another. My folder structure is one parent "wesbites" folder that contains a subfolder for each website.

## Script
```shell
# Configuration
$obsidianRoot = "...\Websites"
$gitRoot = "...\websites"

# Get all project folders in the Obsidian Source
$projects = Get-ChildItem -Path $obsidianRoot -Directory

foreach ($project in $projects) {
    $projectName = $project.Name
    $sourcePath = $project.FullName
    $destinationPath = Join-Path $gitRoot "$projectName\content"

    # Check if the corresponding Git folder exists
    if (Test-Path $destinationPath) {
        Write-Host "Syncing: $projectName..." -ForegroundColor Cyan

        # Robocopy flags:
        # /MIR  : Mirrors a directory tree (deletes files in dest that no longer exist in source)
        # /Z    : Copies files in restartable mode
        # /R:2  : Retries twice on failure
        # /W:5  : Waits 5 seconds between retries
        # /XD   : Excludes directories (e.g., local .git or .quartz folders if they exist)
        robocopy $sourcePath $destinationPath /MIR /Z /R:2 /W:5 /XD .git .quartz .obsidian
    }
    else {

        Write-Warning "Skip: Destination '$destinationPath' not found for project '$projectName'."
    }
}

Write-Host "Sync Complete." -ForegroundColor Green
```