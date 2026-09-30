# Working rules for this folder

## Language

- Every file in this repository — notes, code, comments, commit messages, drafts — is written in **English**.
- Chat language does not leak into files. This includes the weekly digest: the chat reply is in Russian, the archived file in `digest/` is in English.

## Layout

| Path | What goes there |
| --- | --- |
| `README.md` | Goal, phases with dates and gate artefacts, **current phase**, status table |
| `PLAN.md` | English mirror of the plan doc (canonical: https://claude.ai/code/artifact/b916a49a-9e9c-4960-bb37-62b0dc0b7612). Re-sync when the doc changes. |
| `LOG.md` | Weekly log, newest entry first |
| `notes/phase-N-*/` | Study notes for that phase; `README.md` holds the topic checklist |
| `labs/<lab>/` | One folder per lab; `README.md` holds goal and definition of done; code, results, notebooks live next to it |
| `writing/` | Drafts of public write-ups, one file per piece, started from `TEMPLATE.md` |
| `digest/` | Weekly quantum-threat digest archive (`YYYY-MM-DD.md`) and `crqc-estimate.md` |
| `sources/` | `bibliography.md` (grouped by phase); `papers/` for local PDFs (git-ignored) |

## Core rule: every phase ends with an artefact

- A phase is closed only when its gate artefact (code, write-up, talk) is **published** and the checkpoint question is passed.
- Reading without producing is drift. If a week has theory hours but no lab or writing progress, flag which artefact is due.
- If a phase overruns by more than a month, trim the next phase; do not shift the whole plan. Phases 1–2 outrank 3–4.

## Updating LOG.md ("log this week")

1. Add a new entry at the top of the log (below the template), using the template: date, phase, hours (by bucket), done, learned, blocked, next week.
2. Tick completed items in the relevant `notes/phase-*/README.md` and `labs/*/README.md` checklists.
3. Update `README.md`: the `Current phase` line, `Last updated`, and the Status column of the phase table.
4. Commit: `Log week N` (plus a short summary line). The commit includes that week's `digest/YYYY-MM-DD.md` files — the scheduled digest task saves files but never commits.

## CRQC estimate

- `digest/crqc-estimate.md` is the single source of truth for the personal CRQC timeline view.
- Change the numbers only on an explicit decision; every change gets a dated entry in its change log with the reason.

## Sources

- Prefer primary sources: NIST FIPS, IETF drafts, arXiv/ePrint papers, vendor engineering blogs.
- When a note cites a press release or news article, also link the underlying paper or standard and note what the headline omits.
- Add every new source to `sources/bibliography.md` under its phase.

## Git and publishing

- The repository is public. Anything committed is visible to everyone: no personal data, credentials, employer-internal material, or copyrighted PDFs (`sources/papers/` is git-ignored).
- Git run from the Cowork sandbox cannot delete files in this folder without a per-session delete permission, so it leaves stale `.git/*.lock` and `tmp_obj_*` files after a commit. After committing from the sandbox, remove them (with delete permission) or commit from the local Git for Windows instead.

## Content rule

- Files are about the subject matter. No personal or biographical notes.
