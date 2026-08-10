# Roadmap — iOS Agent Skills

## Identity

This repository is a reusable iOS/Swift/SwiftUI skill and reference library. It is maintained as a vendor/reference surface, not as an application product lane.

## Vision

Keep selected architectural patterns discoverable, reviewable, and portable for AI coding agents without turning the mirror into an uncontrolled fork or a separate product brain.

## Current phase

Reference maintenance. No active product implementation is selected.

## Now

- Keep the repo-readable instruction and documentation contract healthy.
- Preserve the skill graph and upstream attribution.

## Next

| ID | Slice | Trigger | Acceptance |
|---|---|---|---|
| IOS-SKILL-N1 | Validate and pin a selected skill for a consuming project | A concrete iOS project requests one of these patterns | Review against the target SDK/toolchain and import only the bounded selected material with attribution |
| IOS-SKILL-N2 | Reconcile an upstream refresh | A reviewed upstream release materially improves the reference set | Diff, review, preserve local instruction surfaces, and push a clean bounded update |

## Later

- Add locally proven iOS patterns only when they are general, attributed, and independently useful.
- Improve portability and skill-selection metadata when a real consumer exposes a gap.

## Parked / not now

- Building an iOS application inside this repository.
- Treating every upstream change as an automatic local update.
- Using this reference repo as a Kanban/product roadmap without explicit adoption.

## Direction locks

- Preserve upstream attribution and license boundaries.
- Validate patterns against the consuming project's actual SDK and architecture before adoption.
- `TASKS.md` is current execution truth; `BACKLOG.md` is not an automatic queue.

## Review cadence

Update after a reviewed upstream sync, a selected skill adoption, or an explicit repository-governance change.
