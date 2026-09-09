# TheOdinProject/curriculum context
> refreshed 2026-09-09 | upstream default: main @ dcf223def8fd7b7862dfd1055e6b15136020bc6f

## Identity & policies
- upstream: TheOdinProject/curriculum, default branch `main`, primary language: Markdown (JS tooling for linting). English-first (all lessons in English).
- CLA/DCO: none (no CLA bot, no DCO found in CONTRIBUTING or .github).
- AI-assisted PR policy: unstated (no ban found; no disclosure requirement).
- signed commits required: no.
- PR template: none in repo root or .github (vetted policy `pr_template_present: false`). Use pipeline 3-section fallback body.
- external tracker: github.

## Conventions (verified from merged PRs)
- branch naming: mixed — `patch-N`, `fix/...`, `chore/...`, `update-...`, `feat/...`. No dominant pattern; use `fix/<kebab-description>`.
- commit style: plain imperative / descriptive subjects (e.g. "Update knowledge check to prevent misunderstandings").
- test command: `npm run lint -- "./path"` (markdownlint-cli2); `npm test` (node --test). CI: codespell + markdownlint + labeler + stale.
- how outside PRs merge: very responsive; 65 external merges in 60d; typo/grammar/simple-syntax fixes explicitly welcomed without a prior issue (CONTRIBUTING "Simple Issues and Changes").

## Maintainer picture
- Active maintainers; high external-merge throughput. Areas in flight: Prisma v7 updates, JS lesson updates, debugging lesson, knowledge-check clarifications.

## Issue-area health
- Typo/grammar/link fixes are the "Easy Fix" category and are welcomed directly via PR (no issue needed for simple changes).
- Avoid significant content changes without maintainer approval.

## Gap ledger (dedupe — READ FIRST, never re-pick)
- `2026-08-04` self-found docs-grounded fix — pr-opened (fork PR #1).
- `2026-08-24` issue #31330 (stale "Additional Resources section below" sentence) — pr-opened (fork PR #16), closed 2026-09-09 (lesson file removed upstream; no longer relevant).

## Mined gaps (discovered, not yet attempted)
- (this run) trivial-fix pass: hunt typos, dead/broken links, stale command references, wrong doc lines across the whole repo; pack >=3 genuine fixes into <=10 files.
