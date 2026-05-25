# AGENTS.md — iosagentskills
## Project anchor
- Knowledge anchor: `/home/openclaw/knowledge/projects/iosagentskills.md`


<!-- HERMES-PROJECT-CONTEXT:START -->
## Shared project context contract
- Knowledge anchor: `/home/openclaw/knowledge/projects/iosagentskills.md`
- Repo path: `/home/openclaw/projects/iosagentskills`
- Execution truth in this repo:
- `TASKS.md`
- `repo-local docs`
- `versioned skill/reference artifacts`
- Harness mirrors: repo-root `AGENTS.md`, `.hermes.md`, `.codex/AGENTS.md`
- Telegram: use the dedicated bound topic for the active lane when one exists; otherwise bind/create one before treating chat as canonical truth.
- Kanban: only canonical if the knowledge anchor explicitly says this lane adopted a board/task contract.

## Method defaults
- planning/spec -> gstack `/office-hours` + `/autoplan`
- review -> gstack `/review`
- security review -> gstack `/cso`
- investigation/debug -> gstack `/investigate`
- browser QA -> gstack `/qa` or `/qa-only`
- land/deploy -> gstack `/ship` or `/land-and-deploy`

## Boundaries
- Do not treat chat history alone as project truth when the knowledge anchor and repo canon exist.
- Do not assume Codex.app or local Mac/WSL sessions use Kanban as truth unless the anchor explicitly says so.
<!-- HERMES-PROJECT-CONTEXT:END -->

## Repo-specific notes
- Keep additional repo-specific details below this managed contract if they do not conflict with the shared anchor.

## Branch/worktree discipline
- This instruction contract must exist on the active branch/worktree, not only `main`.
- Before code changes: run `git fetch --prune`, `git status -sb`, `git branch -vv`, and `git worktree list`.
- Keep docs-only instruction cleanup commits separate from implementation commits; never use broad `git add -A` for mixed cleanup/code drift.
- If branch/upstream/worktree state is behind, diverged, detached, or dirty with unrelated files, report branch/worktree drift before coding or handoff.

## Donald/Mac/Codex.app
- DonaldMacbook, Codex.app, and Mac-local shells must read this file first and then follow the knowledge anchor.
- Mac-local screenshots, builds, device/Vectorworks proof, and receipts are evidence surfaces, not a separate canonical project brain.
- When acting on an explicit Mac handoff, return concise `accepted`, `blocked`, or `done` with evidence.
