# ANNA — the data analyzer
*(named by the owner, 2026-07-30: "its not really isaac. its a
subset of his abilities. We can call it anna, for analyzer.")*

Anna is the commercial data-analysis product built on the Isaac
engine. She is a subset of his abilities with a storefront around
them — not him, never fed back into him, no live mind anywhere in
this repo.

## The family

- **isaac dc** — the datacenter live version (the engine, the
  promoted wall, the business machinery). Anna calls its CLI — a
  verbatim copy is bundled at `engine/` so this repo stands alone
  (`engine/ENGINE_PROVENANCE.md` records the source commit).
- **isaac-paperclip** — research.
- **anna** (this repo) — the product: reports a client pays for.

## What Anna does

One command turns a messy real-world CSV into a client-ready
report: `report.html` with a KPI band, ranked headlines with
so-what lines, month-over-month with YoY, segments, seasonality
(validated out-of-sample), correlations (shared-trend caution),
concentration, customer base, at-risk customers, coupons, baskets,
returns/reversals with event detection, order whales,
reconciliation (the book that doesn't balance, by row), charts —
and the full receipts beneath. Two tiers of claims, never
conflated: a **certified rule** (the engine's strictest courts) and
a **what's-there description** graded SOLID / WEAK / UNSTABLE by
200 random half-samples plus a persistence test. Where the data
can't support a claim, Anna says so instead of guessing — that
honesty is the product.

    python honest_report.py client.csv --brand "Your Name"
    python honest_report.py client.csv --time date --no-audit
    python honest_report.py client.csv --narrative note.txt
    python honest_report.py client.csv --window 2026-06-01 2026-06-14 --window-label "the promo"
    python clean_file.py dirty.csv --resolution revenue=2.5

Requires: Python 3.12+ and `pip install -r requirements.txt`
(numpy, matplotlib). The engine is bundled in `engine/` — Anna is
standalone. `ISAAC_ENGINE_DIR` still overrides the bundled copy,
and a sibling `dc/` clone remains the fallback for the old
two-repo layout. Delimited text only — Excel refused with
instructions, never garbage.

## The record behind her

Every organ passed a planted-truth court AND a blind court on real
unseen data (25k UCI Online Retail; 20k NYC 311), with findings
validated by independent recomputation — including naming a
−52,784 fee-reversal source to the pound and a one-day event
carrying 87% of all negatives. The full history, courts, and the
lens-loop research direction live in `dc/docs/` (see
SESSION_HANDOFF_2026-07-30_INCOME_AND_LENS.md and
DESIGN_LENS_LOOP_2026-07-30.md).

`portfolio/` holds the sample deliverables and `GIG_COPY.md` the
offers, prices, and paste-ready listings.
