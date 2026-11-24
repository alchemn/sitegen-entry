# sitegen-entry

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/alchemn/sitegen-entry/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/alchemn/sitegen-entry/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)

A faster drop-in for makefun-site 1.0.0: `solve.js` answers every case with
exactly the output tree makefun-site's `build` returns — same front matter
refusals, same slug and permalink rules, same Markdown rendering, same
template dialect, same report — but builds it in single passes: bodies are
read as line arrays instead of re-split strings, templates are parsed once
per case into a node tree and rendered into one joined buffer, slugs and
long dates are cached, and inline text is escaped in bulk runs instead of
one character at a time.

`main.ts` is the harness driver: it reads every case from
`/input/cases.json`, answers each with `run`, and writes
`/output/answers.json`.
