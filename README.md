# PQC Lab

A 12-month plan to build expertise in post-quantum cryptography (PQC) and quantum computing.

**Goal:** by 2027-09-30, be a credible candidate for PQC migration engineer / cryptography engineer roles, with a portfolio of one real migration, a cryptography inventory tool, public write-ups, and an open-source contribution. Budget: 8–12 h/week (~450 h/year).

**Plan document (canonical):** https://claude.ai/code/artifact/b916a49a-9e9c-4960-bb37-62b0dc0b7612 — mirrored in [PLAN.md](PLAN.md).

## Status

**Current phase: 1 — PQC foundations (Oct–Dec 2026)**

Last updated: 2026-09-30 (Week 0, project set up)

## Phases and gate artefacts

A phase is closed only when its gate artefact is published **and** the checkpoint question is passed.

| # | Phase | Dates | Gate artefacts | Checkpoint | Status |
| --- | --- | --- | --- | --- | --- |
| 1 | PQC foundations | Oct–Dec 2026 | OQS hybrid-TLS bench with measurements ([labs/oqs-tls-bench](labs/oqs-tls-bench/)); teaching ML-KEM in Python ([labs/mlkem-python](labs/mlkem-python/)); write-up "What actually changes in the TLS handshake with ML-KEM" | ML-KEM vs ML-DSA; why hybrid; what breaks with 5× certificates | Not started |
| 2 | Migration in real systems | Jan–Mar 2027 | Alpha Clarity PQ migration; CBOM inventory tool ([labs/cbom-tool](labs/cbom-tool/)); migration write-up | Migration plan for an unfamiliar system in one hour | Not started |
| 3 | The quantum side | Apr–Jun 2027 | Stim surface-code notebook ([labs/stim-surface-code](labs/stim-surface-code/)); P-256 resource estimate (Azure QRE + Qualtran); revised CRQC estimate | Press release → primary source → which blocker moves, in 10 minutes | Not started |
| 4 | Niche and market | Jul–Sep 2027 | Blockchain CRQC analysis; OSS contribution; meetup/conference talk; rebuilt CV | ≥3 inbound PQC interviews or consulting requests | Not started |

## Layout

| Path | Contents |
| --- | --- |
| [PLAN.md](PLAN.md) | Full plan (English mirror of the doc) |
| [LOG.md](LOG.md) | Weekly log |
| [CLAUDE.md](CLAUDE.md) | Working rules for this folder |
| [notes/](notes/) | Study notes per phase, with topic checklists |
| [labs/](labs/) | Hands-on lab projects, each with a goal and definition of done |
| [writing/](writing/) | Drafts of public write-ups ([TEMPLATE.md](writing/TEMPLATE.md)) |
| `digest/` | Weekly quantum-threat digest archive and CRQC estimate — local only, not published |
| [sources/](sources/) | [bibliography.md](sources/bibliography.md) and local copies of papers |
