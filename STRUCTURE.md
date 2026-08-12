# How this repo is organized (owner spec, 2026-08-12)

Three areas, hard walls between them, so different files never mix.

```
core/      her standing self: the analysis code and the general rules
           she has earned. Nothing client-specific ever lands here.
  rules/   generalized discoverable rules — knowledge proven on past
           jobs that applies to ANY future job. Promoted in, never
           copied from a client's numbers.
tools/     runnable utilities she uses on jobs (the cleaner today;
           the scanner and the rule-checker when they are promoted).
engine/    the bundled Isaac engine (verbatim copy of dc — see
           engine/ENGINE_PROVENANCE.md). Not hers to edit.
jobs/      the work. One folder per JOB. A job may hold several
           datasets, files, or subgroups — each dataset gets its own
           subfolder inside the job. Jobs are INDEPENDENT: nothing
           in one job may read from or write to another.
  portfolio/   the storefront samples (a job like any other).
```

## The rules of the walls

1. **Jobs are independent.** Every deliverable for a dataset lands in
   `jobs/<job>/<dataset>/`. Client data never enters core, never
   enters another job, and never enters any live mind (standing law).
2. **What flows upward is rules, not facts.** A discovery made on a
   job may be promoted into `core/rules/` ONLY if it is general —
   true of tables, not of that client. "Orders, not rows" is a rule;
   a client's December numbers are facts and stay in their job.
3. **The sequence is recoverable.** A job folder is a timeline: the
   files as received, then what was done, in order, with logs. The
   rebuilt-table output (the three-layer deliverable, being built)
   keeps each row's original feed position as a column.

## Running her

    python core/honest_report.py client.csv --job smith-co --brand "Your Name"
    python tools/clean_file.py dirty.csv --resolution revenue=2.5

Without `--job` the report files under `jobs/portfolio/` (the samples).
