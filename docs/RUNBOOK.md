# Runbook - code-reading-quest

Status as of 2026-10-05, derived from the repo and its git history. Items the repo cannot answer are marked `[DO UZUPEŁNIENIA przez Kamila: ...]`.

## What runs where

- This is a plain content repository: Markdown session files in `sessions/`. No server, build, CI or hosting configuration exists in it (no `.github/`, no site config).
- Sessions are produced by an automated daily process outside this repo (see the README, "How it works") and committed directly to `main`, one commit per session, message format `docs: S<N> <short English summary>`.
- Public hosting beyond GitHub itself (for example a rendered site): none configured in the repo. `[DO UZUPEŁNIENIA przez Kamila: czy istnieje strona publiczna poza GitHubem]`.

## Publishing a session

1. Create `sessions/YYYY-MM-DD-S<N>.md`, where `<N>` continues the sequence (latest in the repo at the time of writing: S84, 2026-10-02). Use an existing session as the template: concept, story, snippets, `Verified` block with real interpreter output, quiz with keys, spaced-repetition card.
2. Run every snippet (`node` / `python3`) and paste the real output into the verified block. Do not publish a session whose output was not executed; this is the repo's core promise.
3. Commit to `main` with `docs: S<N> <summary>` and push. `[DO UZUPEŁNIENIA przez Kamila: ewentualne wymagania co do pushu na main, jeśli ochrona gałęzi zostanie włączona]`.

Sequence notes: day gaps in the session numbering dates are normal (not every day produces a session). Sessions S36-S58 were removed from the working tree one per new session (2026-08-12 to 2026-09-07); they remain in git history, and no session has been removed since.

## Rollback and corrections

- A wrong answer key or claim: publish a correcting commit to the same file (precedents in history: `S51` answer key, `S67` timing claim). Do not rewrite history.
- A bad session file: `git revert <commit>`.
- Content scan before publishing: check for stray non-Latin characters and for anything private (precedent: a stray Cyrillic character in a diagram, fixed in `99f7904`).

## Secrets and data

- The repo needs no secrets and must not contain any: no keys, tokens, notification topics, client names or personal data in session files. The session state, progress and answer history live in a private store, not here.
- The repo is public; treat every commit as permanent.

## Common problems

| Symptom | Cause | Action |
|---|---|---|
| A reader reports a different output than the key | environment-dependent snippet (Node/Python version, locale, timezone) | re-run the snippet, state the version or make it deterministic, publish a correction |
| Session number or date breaks the sequence | process skipped a day or ran twice | keep numbering monotonic; do not rename published files |
| Push to `main` is refused | a local pre-push guard or a remote protection rule | `[DO UZUPEŁNIENIA przez Kamila: obowiązujący sposób pushowania do tego repo]` |

## Monitoring

None in the repo. The only freshness signal is the date of the latest commit. `[DO UZUPEŁNIENIA przez Kamila: kto sprawdza, że codzienny proces opublikował sesję]`.
