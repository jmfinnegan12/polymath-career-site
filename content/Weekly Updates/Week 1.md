# Week 1 - 4/6/2026

This week I got my ducks in a row for starting this project and the other three projects I am actively working on.

For each project I chose a name and wrote a brief description including the main goal, background, and why it interests me. 

I created a prototype website for each project. Currently I'm just using the descriptions I wrote as an "about" page placeholder until I get more content on each website. I bought the domain names and I set up my websites using Quartz and Obsidian. Quartz is a static site generator that converts markdown into websites. Obsidian is my preferred notetaking app--it is markdown native, so I can easily connect my notes to my websites.

My Obsidian vault contains journal entries, schedules, business ideas, and other miscellaneous notes that I want to keep private. I believe that minimizing [[context switching]] is crucial to staying productive, especially when starting new projects with unfamiliar workflows. Otherwise the project will be nearly impossible to maintain. I needed a solution that would keep my personal notes private but enable me to edit my website content in Obsidian, which I am already familiar with and use extensively. 

I decided that the best solution is to edit and store my website content within dedicated subfolders in my Obsidian vault, then mirror the content of those folders to their respective GitHub repos where Quartz is set up to generate the site. This way I can edit my websites in Obsidian and simply run a script to publish them. No new platforms, no manual copy/paste, the process is short and familiar.

I set up a subfolder of my vault for my websites. Then I had Gemini write me a powershell [[Transfer Script|script]] that mirrors folder contents to my local GitHub repos. When I run the script I can preview changes to the site locally, and when I am ready to publish I sync Quartz and it takes care of publishing. I am still refining the [[Website Update Workflow|workflow]], but I am happy with this as a low barrier to entry and decently scalable starting point.

Right now my sites are live and working, which was my main goal for the week. They are still placeholder default layout. I am looking forward to playing with design and formatting elements next week, as well as getting to work on the prototypes for my other projects!