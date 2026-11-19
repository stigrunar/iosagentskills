# AGENTS.md — iosagentskills

## Coordination and context

Use Linear for work, future requests and relevant work notes. Search for an existing issue before creating one; record the responsible agent, actual executor, status, next action and verified result. Link repo plans and evidence to that issue. BACKLOG.md may retain technical detail with Linear links, not a separate queue. ROADMAP.md records direction; TASKS.md preserves technical continuity; CHANGELOG.md records delivery.

Use GBrain for relevant knowledge and decisions; the shared repository is `stigrunar/gits-knowledge`. Find this project's knowledge by its existing anchor `projects/iosagentskills.md`; verify the current source location. Preserve existing source IDs and privacy boundaries. Resolve local paths on the current host rather than assuming historical Mac/Linux paths.

Own the authorized outcome through verification. Delegate the goal, context, scope and acceptance evidence to one executor per overlapping scope; continue independent work when blocked. Use relevant available skills, not a mandatory tool choreography. Keep instructions separate from task logs.

## Read when relevant
- `README.md` — upstream-authored library overview and skill graph.
- `ROADMAP.md` — selected local maintenance direction.
- `BACKLOG.md` — technical idea detail linked to Linear.
- `TASKS.md` — technical continuity and evidence.
- `CHANGELOG.md` — accepted local mirror/governance history.
- `docs/AGENTS.md` — scoped documentation placement and freshness rules.

## Repository role
This is a reusable iOS agent-skill/reference library, not an application product lane. Validate selected patterns against the consuming project's actual SDK and architecture before adoption.

## Branch/worktree discipline
- This instruction contract must exist on the active branch/worktree, not only `main`.
- Before code changes: run `git fetch --prune`, `git status -sb`, `git branch -vv`, and `git worktree list`.
- Keep docs-only instruction cleanup commits separate from implementation commits; never use broad `git add -A` for mixed cleanup/code drift.
- If branch/upstream/worktree state is behind, diverged, detached, or dirty with unrelated files, report branch/worktree drift before coding or handoff.

## Outcome specification gate

- Before a Linear-selected outcome becomes an implementation task, record `spec_required: true|false` with a one-line reason in the roadmap item, `TASKS.md`, or the explicit handoff.
- Set `spec_required: true` for work spanning multiple sessions/owners, multiple user journeys, product/design decisions, API/data/schema/permission/runtime contracts, cross-repo or subsystem boundaries, security/privacy risk, prior intent drift, or acceptance that must survive chat loss.
- When required, run/follow `to-spec`, freeze the contract under the repo's existing spec convention or default `docs/specs/<spec-id>-<slug>.md`, and link the exact path and revision from `ROADMAP.md`, `TASKS.md`, and any implementation handoff before work starts.
- A small bounded change may use `spec_required: false` only when acceptance is explicit in `TASKS.md` or the handoff.
- Never create placeholder specs or an empty `docs/specs/` directory; a root `SPEC.md` is not a universal convention.
