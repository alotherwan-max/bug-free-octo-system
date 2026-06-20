# Claude Code Instructions

## Git Workflow

**Every run must: commit changes on a branch → create a PR → merge to `main`.**

### Steps for each run

1. **Branch** — work on a new or existing branch (not `main` directly)
2. **Commit** changes with a clear message
3. **Push** the branch: `git push -u origin <branch-name>`
4. **Create PR** via GitHub MCP (`mcp__github__create_pull_request`) targeting `main`
5. **Merge PR** via GitHub MCP (`mcp__github__merge_pull_request`) using squash merge

### Branch naming

Use the session-designated branch if one is provided in the session instructions (e.g. `claude/dazzling-galileo-471fov`). Otherwise use a timestamped name: `auto/update-YYYYMMDD`.

### PR format

- Title: `Auto-update: <short description> <date>`
- Body: bullet-point summary of what changed + sources used
- Merge method: `squash`

### If main is ahead of the branch

Fetch and rebase before creating the PR:
```
git fetch origin main && git rebase origin/main
```

### Never

- Push directly to `main`
- Skip the PR step
- Leave changes only on the feature branch
