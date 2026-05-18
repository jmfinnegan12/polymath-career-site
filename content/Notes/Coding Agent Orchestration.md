# Coding Agent Orchestration

A system for running coding agents against real project work, with Obsidian as the shared substrate. The agents do not just answer questions — they execute against specs I write in the vault, then write their work logs and handoff notes back into the same vault files when they finish.

The pieces:

**Project management docs.** Each major project has a project management note that tracks active initiatives, planned projects, and what is in flight. Same template across all of them.

**Initiative and project templates.** Anything new gets stood up from a template — same frontmatter, same structure, same place for status and links. Means an agent looking at a project file always finds the same shape.

**Dataview tables.** Each project management doc has Dataview queries that organize projects by status and initiative.

**Spec-driven development.** Real building starts with a spec, brainstormed in Obsidian with [[Claudian]] using the brainstorming skill from the [superpowers](https://github.com/obra/superpowers) framework. Once the spec is clear, I hand it off to a coding agent.

**The CLAUDE.md handoff.** My repo-level CLAUDE.md tells agents where the vault lives on disk and how to find specs. They read the spec, do the work in code, then come back to the vault and append work logs and handoff notes to the relevant project file.

The result is that the project files in Obsidian stay the source of truth for what has been done and what is next. New sessions pick up where old ones left off. The time I used to spend figuring out where I left off and how to get going again is mostly gone — the agents leave the breadcrumbs themselves.
