# Claude Code Instructions

## Git Workflow

**Always push directly to `main`.** Do not create feature branches or pull requests unless the user explicitly asks for one.

- Work on `main` locally
- Push with: `git push origin main`
- If `main` is behind the remote, fetch and merge first: `git fetch origin main && git merge origin/main`, then push
- Never create a PR or suggest one unless the user requests it
