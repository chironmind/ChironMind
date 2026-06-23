# AGENTS.md

Guidance for coding agents in this repository. This file is self-contained.

ChironMind is a profile/landing repository: a README.md (a GitHub-profile-style index page) plus a banner image that links out to the Centaur Technical Indicators projects. It contains no source code, build system, or tests.

## Build & test

There is no build, test, or lint tooling in this repository — it is documentation/content only (`README.md` and `assets/`). There is no pre-change gate to run. **Flag:** if a task assumes a build or test step here, stop and confirm scope, because none exists.

The only meaningful check after editing the README is that Markdown renders and that linked images and URLs resolve.

## Working rules

- Make the smallest safe diff that satisfies the task.
- No opportunistic refactors or unrelated content rewrites.
- Preserve the existing file organization and naming (`README.md`, `assets/`).
- Keep image references and external links intact unless the task is specifically to change them.
- Stage only the files your task names. Never use `git add .` or `git add -A`.

## Never guess

If information is missing, the task is ambiguous, or two implementations are plausible, STOP and ask for input before proceeding. Do not assume intent, invent links/URLs, or fabricate project descriptions.

## Stop-and-report

Surface the blocker (do not work around it) when:

- A task assumes a build/test/lint gate that this repository does not have.
- The task would require a breaking change (e.g. removing or renaming `README.md` or `assets/`) without explicit approval.
- Instructions conflict with the repository's actual state (content-only, no code).
