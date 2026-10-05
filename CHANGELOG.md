# Changelog

Format: [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). The repo has no version tags; entries are grouped by date. Each daily session is one commit (see `git log`); only notable changes are listed.

## [Unreleased]

### Added
- Handover documentation: `docs/RUNBOOK.md`, a repository layout section in the README, this changelog.

### Fixed
- README: "most recent dozen published" replaced with the actual published range (S59 onward).

## 2026-09-02 to 2026-10-02

### Added
- Sessions S64-S84 (function-call boundary, call-site `this`, event-loop queues, promise combinators, `AbortController`, spread and `forEach` pitfalls, structured-output validation, RAG context selection, default parameters, comparison rules, header and `.env` strings, error logging as JSON).
- `d2590e8` (2026-09-06): MIT license.

### Changed
- From S68 on, older sessions are no longer removed when a new one is added (see below).

### Fixed
- `b1ededc` (2026-09-05): S67 timing claim corrected (`allSettled` is slower on failure), verified `AggregateError` limits added.
- `99f7904` (2026-09-07): stray Cyrillic character replaced in the S68 diagram.

## 2026-08-02 to 2026-09-01

### Added
- Sessions S36-S63, one per day (shallow copies, `-0`, `includes` vs `indexOf`, key order in `JSON.stringify`, loose equality, string coercion in `+`, chained comparisons, `null` checks, defaults, optional chaining, `typeof`, `parseInt` vs `Number`, floating point, large integers, dates and time zones, Unicode normalization, `switch`, invisible characters, JSON round-trip, `sort()`, `const`).
- `1e91029` (2026-08-11): README documents the pipeline architecture and fixes the session counter.

### Changed
- Publication window: each new session removed the oldest one from the working tree (S36 through S58, between 2026-08-12 and 2026-09-07). Removed sessions remain in git history.

### Fixed
- `5ff15fb` (2026-08-18): S51 answer key corrected (two entries misread, not three).
