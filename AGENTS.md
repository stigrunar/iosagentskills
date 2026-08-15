# AGENTS.md — iosagentskills
## Project anchor
- Knowledge anchor: `projects/iosagentskills.md` in `stigrunar/openclaw-knowledge`
- Hermes host checkout: `/home/hermes/knowledge/projects/iosagentskills.md`

## Canonical read order
- `README.md` — upstream-authored library overview and skill graph.
- `ROADMAP.md` — selected local maintenance direction.
- `BACKLOG.md` — unselected candidates and review findings.
- `TASKS.md` — current local execution truth.
- `CHANGELOG.md` — accepted local mirror/governance history.
- `docs/AGENTS.md` — scoped documentation placement and freshness rules.

## Repository role
This is a reusable iOS agent-skill/reference library, not an application product lane. Validate selected patterns against the consuming project's actual SDK and architecture before adoption.

<!-- HERMES-PROJECT-CONTEXT:START -->
## AGENTS hygiene

Keep this file lean: project identity, canonical context links, owner/route boundaries, safety rules, and durable workflow invariants only. Do not use `AGENTS.md` as a changelog, run log, task history, acceptance receipt store, or scratchpad; move delivered history to `CHANGELOG.md`, active execution to `TASKS.md`, receipts/logs to `docs/receipts/` or `docs/reports/`, and broader durable policy to `/home/hermes/knowledge`. `ROADMAP.md` `Now` is current/selected next work only; accepted/delivered slices move to `CHANGELOG.md`, with at most a compact `Recently completed` pointer outside `Now`.
## Shared project context contract
- Knowledge anchor: `projects/iosagentskills.md` in `stigrunar/openclaw-knowledge`
- Hermes host checkout: `/home/hermes/knowledge/projects/iosagentskills.md`
- Hermes host repo path: `/home/hermes/projects/iosagentskills`
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

## Outcome specification gate

- Before a selected `ROADMAP.md` outcome becomes an implementation task, record `spec_required: true|false` with a one-line reason in the roadmap item, `TASKS.md`, or the explicit handoff.
- Set `spec_required: true` for work spanning multiple sessions/owners, multiple user journeys, product/design decisions, API/data/schema/permission/runtime contracts, cross-repo or subsystem boundaries, security/privacy risk, prior intent drift, or acceptance that must survive chat loss.
- When required, run/follow `to-spec`, freeze the contract under the repo's existing spec convention or default `docs/specs/<spec-id>-<slug>.md`, and link the exact path and revision from `ROADMAP.md`, `TASKS.md`, and any implementation/Kanban handoff before work starts.
- A small bounded change may use `spec_required: false` only when acceptance is explicit in `TASKS.md` or the handoff.
- Never create placeholder specs or an empty `docs/specs/` directory; a root `SPEC.md` is not a universal convention.
