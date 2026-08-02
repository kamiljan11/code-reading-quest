# Code Reading Quest

**Predict the output before you run it.** A daily code-reading discipline with spaced repetition and verified outputs — 36+ sessions and counting.

Every snippet in this repo was run through a real interpreter (`node` / `python3`) before the answer key was written down. No guessed outputs.

## Motivation

I build and operate production systems for my own companies in Iceland (a 13-stage quote-to-order pipeline, a freight marketplace, a multi-market pricing SaaS) — most of it shipped with heavy AI assistance. That workflow has one bottleneck: **you can only trust AI-written code as far as you can read it.**

I tried passive tutorials; they didn't stick. What stuck was the loop borrowed from learning science: recall from memory, predict the output cold, verify against a real run, quiz without hints, bank a spaced-repetition card. This repo is the public trail of that loop — one session per day.

## Quick Start

1. Open any file in [`sessions/`](sessions/).
2. Read the snippet. **Write down your predicted output before scrolling further.**
3. Compare with the `verified` block (actual interpreter output).
4. Wrong? Good — that gap is the lesson.

## Usage

Each session file contains:

- **Concept** — one atomic idea (e.g. shallow copy via spread sharing nested references)
- **Encounter** — two related snippets wrapped in a scenario, with a question in one of six rotating formats (predict-output, bug-hunt, what-if, order-of-execution, ranking, reverse)
- **Verified output** — exact interpreter output, run before publishing
- **Quiz** — three no-hint questions with keys
- **Card** — the spaced-repetition card banked from the session (SM-2 scheduling)

The wider system (progress state, encounter bank, review cycles) lives in a private Obsidian vault; this repo is the daily public artifact.

## Contributing

This is a personal practice log, so PRs aren't expected — but the format is free to steal. Fork it, delete `sessions/`, and start your own chain. The only rule that matters: **never look at the output before you've committed to a prediction.**
