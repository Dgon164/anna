# STOPGAP — this branch is not a final version

Branch `stopgap-v0`, opened 2026-08-16 at the owner's direction. It exists so
the current working state of Anna is pushed and shareable while the real
build (the gated fixes below) is decided and done. Nothing on this branch is
claimed to be finished. Treat every capability here as *what she can do today*,
measured, with the limits stated.

## What is on this branch (all committed on main first)

- Anna runs standalone — the engine she calls is bundled at `engine/`
  (a verbatim copy of the dc engine at commit 02db3b8; provenance in
  `engine/ENGINE_PROVENANCE.md`).
- Organized into `core/` (her code + `core/rules/GENERAL_RULES.md`, the
  general rules earned so far), `tools/` (the cleaner), `engine/`, and
  `jobs/` (one folder per job; jobs never mix; `--job NAME` routes output).
  See `STRUCTURE.md`.
- The storefront samples live in `jobs/portfolio/`; the offers in
  `GIG_COPY.md`.

## What is measured but NOT yet fixed here (the benchmark record, 2026-08-12)

Measured on constructed files with known contents, plus real files:

- **Drifting data fools her grading.** Random-walk files earned 8 false SOLID
  labels; the month-of-year check invented a monthly pattern on 6 of 9
  known-shape files (including a plain steady rise). Fix proven in the lab
  (grade time-based claims on separate stretches of time, not random halves)
  — not installed.
- **Combined shapes are missed.** Of nine planted shapes (peak, one-day step,
  slope change, trend + weekly rhythm, two regions cancelling, a slow wave,
  a random walk, two steps, a plain trend) her current tools were fully
  correct on 0; a lab shape-reader prototype names or correctly refuses all
  nine — not installed.
- **She cannot tell when her engine fails** (an empty-but-clean report ships);
  date-keyed tables get no line charts; "last month" trusts file order.
- **Her intake notes cannot reproduce the original file** (15 of 30 test lines
  recoverable). The 10-item receipts rule that fixes it is written, not
  built.
- **Speed at real scale.** Her engine's cycle search grows with the square of
  the row count (it checks every lag up to a third of the rows and repeats
  on 20 shuffled copies). A 25,000-row file took 13 minutes; a 1,067,371-row
  real retail file was projected at days and stopped. The bounded remedy is
  known (cap the lag search, sample the shuffle comparison, transform-based
  rhythm search) — not applied.
- No null-filling option yet (per-column defaults and client-supplied
  prototypes are specified for the build).

## What is safe to use now

The cleaning path (`tools/clean_file.py`): mechanical fixes with a full
changelog, judgment flags never auto-applied, binary files refused with
instructions. Its measured record is clean. Report-tier claims should be read
with the limits above in mind — the strictly-certified tier (the engine's own
rules) produced zero false certifications on every garbage file tested; the
graded-description tier is where the drift weakness lives.

## Where the real work is tracked

`Desktop\Isaac\CHECKLIST.md` (the owner's tracker) — Path A is the gated build
that turns this stopgap into the income-grade version.
