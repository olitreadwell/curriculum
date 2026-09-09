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
- `2026-09-09` self-found trivial-fix pass (typos + dead links) — pr-opened (fork PR #30, branch fix/typos-and-dead-links). 10 fixes / 5 files: 2 dead links replaced (devhints.io/rspec -> rubypigeon rspec cheat-sheet; blog.techatpower.com guard-clause post -> rubystyle.guide guard-clauses) + 8 grammar/typo fixes (its/it's, Rails/Rail's, we're/were, to the following, how you can leverage). Dropped 2 RSpec files with 4 more verified dead-link fixes because they already fail markdownlint on originals (139 pre-existing errors) and CI lints changed files. Rejected false positives: codepen.io 403 (bot-block), support.google.com/marketplace.visualstudio.com 404s (200 with browser UA), web.archive.org 200, transient ERR. Fork CI green (codespell, markdownlint, triage).
- `2026-09-09` self-found trivial-fix pass (typos + grammar) — pr-opened (fork PR #31, branch fix/typos-and-grammar). 4 fixes / 4 files: deployment.md missing article (deploy database -> deploy a database); working_with_apis.md double-colon typo (this:: -> this:, from #31353); dual_boot.md missing preposition (instructions this guide -> instructions in this guide, from 111d00010); managing_ruby_projects.md missing space (e.g.starts -> e.g. starts, from #31312). All meaning-preserving single-token fixes, no rewording/refactor/whitespace churn, US-English dialect respected. Rejected false positives: UK spellings (behaviour), MDN Normal_Flow 301 (not broken), pinned-SHA GitHub links (exist), dead external sites (herokuapp/rawgit/launchschool), Wikipedia paren URLs (work in browsers). Fork CI green (codespell, markdownlint, triage).
- `2026-08-24` issue #31330 (stale "Additional Resources section below" sentence) — pr-opened (fork PR #16), closed 2026-09-09 (lesson file removed upstream; no longer relevant).

## Mined gaps (discovered, not yet attempted)
- (this run) trivial-fix pass: hunt typos, dead/broken links, stale command references, wrong doc lines across the whole repo; pack >=3 genuine fixes into <=10 files.
