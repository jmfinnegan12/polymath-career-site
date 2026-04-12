# Manual Workflow
## 1. Sync Obsidian notes to local GitHub folder
run the sync script
```shell
1. cd Documents\Work\websites
2. .\sync_quartz.ps1
```

## 2. Preview site(s)
quartz build for `project-a`
```shell
1. cd Documents\Work\websites\project-a
2. npx quartz build --serve
```

check `http://localhost:8080` in browser
- quartz will watch for changes

## 3. Push to GitHub
for simple updates:
- `npx quartz sync`
- this pulls changes from remote and pushes local to GitHub
- will not allow for selecting individual files or titling commits

future - for complex redesigns where I want to title and track changes or choose specific files:
- use git add commit push commands