# TheOdinProject/curriculum context
> refreshed 2026-09-25 | upstream default: main @ 09821c0fa (fork main synced 2026-09-25)

## Identity & policies
- upstream: TheOdinProject/curriculum, default branch `main`, primary language: Markdown (JS tooling for linting). English-first (all lessons in English).
- CLA/DCO: none (no CLA bot, no DCO in CONTRIBUTING or .github).
- AI-assisted PR policy: unstated (verified 2026-09-25 against CONTRIBUTING.md, .github/, and org default TheOdinProject/.github -- no ban, no disclosure requirement).
- signed commits required: no.
- PR template: `.github/PULL_REQUEST_TEMPLATE.md` present (Because / This PR / Issue / Additional Information / Pull Request Requirements). Fill verbatim; title format `location of change: brief description`.
- external tracker: github. CONTRIBUTING welcomes simple typo/grammar/broken-link changes directly by PR without an issue; significant changes need maintainer approval first.

## Conventions (verified from merged PRs)
- branch naming: mixed -- `patch-N`, `fix/...`, `chore/...`, `update-...`, `feat/...`. No dominant pattern; use `fix/<kebab-description>`.
- commit style: plain imperative / descriptive subjects.
- test command: `npm run lint -- "./path"` (markdownlint-cli2); `npm test` (node --test). CI: codespell (skip archive, ignore-words .codespellignore) + markdownlint (lints CHANGED files via tj-actions/changed-files) + labeler + stale. codespell currently clean across the whole active repo.
- how outside PRs merge: very responsive; high external-merge throughput; typo/grammar/simple-syntax fixes explicitly welcomed.

## Maintainer picture
- Active maintainers; high external-merge throughput. Areas in flight (avoid): Prisma v7 updates, JS lesson updates, debugging lesson, knowledge-check clarifications.
- Issue #31401 (Testing Basics article down) assigned direction to ZackHoang (web-archive swap, revisit October); #31408 (Semantic HTML landmarks) is an active content debate; #31391 (ORCA reader) environment-specific, maintainer unable to reproduce.

## Issue-area health
- Typo/grammar/link fixes are the "Easy Fix" category, welcomed via PR without an issue.
- Avoid significant content changes without maintainer approval.

## Gap ledger (dedupe -- READ FIRST, never re-pick)
- `2026-08-04` self-found docs-grounded fix -- pr-opened (fork PR #1; later superseded).
- `2026-09-09` self-found trivial-fix pass (typos + dead links) -- pr-opened (fork PR #30, branch fix/typos-and-dead-links). 10 fixes / 5 files: 2 dead links replaced (devhints.io/rspec -> rubypigeon rspec cheat-sheet; blog.techatpower.com guard-clause post -> rubystyle.guide guard-clauses) + 8 grammar/typo fixes. Dropped 2 RSpec files (rspec_part_one_basics.md, rspec_part_two_code_sharing.md) because they already fail markdownlint on originals (139 pre-existing errors) and CI lints changed files. Fork CI green.
- `2026-09-09` self-found trivial-fix pass (typos + grammar) -- pr-opened (fork PR #31, branch fix/typos-and-grammar, still open). 4 fixes / 4 files. Fork CI green.
- `2026-08-24` issue #31330 (stale "Additional Resources section below" sentence) -- pr-opened (fork PR #16), closed 2026-09-09 (lesson file removed upstream; no longer relevant).
- `2026-09-25` (this run) repo-audit matrix pass -- DROPPED, no verifiable pick (see Mined gaps). Honest outcome: repo heavily maintained; comprehensive link/typo/drift audit found no safe, verifiable, genuine gap.

## Mined gaps (discovered, not yet attempted)
- `2026-09-25` docs/dead-links -- DROPPED. Checked ~1960 unique external URLs across the whole active repo (all courses, excl archive/markdownlint/templates). Only 404-class hits were false positives: launchschool.com/books/* (the whole launchschool.com returns 404 to curl with browser UA incl. homepage -> anti-bot, NOT broken; prior run also rejected it), relishapp.com/rspec/* (genuine 404 but live replacement is rspec.info AND both files rspec_part_one_basics.md already fail markdownlint -> CI would go red -> not safe to touch), MDN rotate3d()/scaleZ() and wikipedia parentheses URLs (extraction artifacts; real URLs return 200), jrsinclair article (transient 503). Medium/StackOverflow/Sitepoint/Pexels/npmjs/codepen 403 = anti-bot, per config false_positive_rules.
- `2026-09-25` docs/drift + factual statements -- DROPPED. Ruby docs-lang version links consistent at en/3.4 across active course (archive only has 3.3/2.7, intentionally frozen); Rails version references (6/7/8) accurate; Node LTS + `min-release-age` npm setting accurate; CRA deprecation already corrected; git commands (rebase/force-push/revert, master-to-main handling) accurate; Vite React scaffold command accurate; Jest/Babel v8 "not yet compatible" parenthetical is hedged ("as of writing"), not demonstrably wrong.
- `2026-09-25` spellcheck -- DROPPED. codespell (repo config, skip archive, .codespellignore) clean across the entire active repo; no remaining misspellings.
