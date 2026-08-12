# The bundled engine — provenance

Copied verbatim from the private repo `github.com/Dgon164/dc` at
commit **02db3b8** (2026-07-31, "UNDERSTANDING DIAGNOSIS CAMPAIGN")
on **2026-08-12**, so Anna runs standalone — no sibling clone, no
environment variable, nothing outside this repo.

## What was copied

| File | Why |
|------|-----|
| `askisaac.py` | the promoted CLI — the only door Anna knocks on (`--analyst`, `--audit`) |
| `isaac.py` | the engine itself; `isaac_store/bridge.py` resolves it as the file sitting beside `isaac_store/` |
| `isaac_store/` | the whole package, tests included (analyst, audit, report, intake, structural, bridge, codec, and the rest) |
| `face.py`, `alpha.py` | imported by two of the package's own tests (`test_face.py`, `test_ops.py`) so the bundled copy can verify itself |

## What was NOT copied

`promote.py` / `worker.py` (dc's own promotion machinery), `demos/`,
`experiments/`, `research/`, `lens_research/`, `docs/`, `spatial/`,
`standalone/`, `ui/` — none of it is needed to run the two faces Anna
calls. The research record stays in dc, which remains the engine's
home; this folder is a reader's copy, not a fork.

## The standing laws honored here

- **Anna carries NO live mind.** Nothing in this folder reads or
  writes any `mind.isaac`. The mind-touching options of `askisaac.py`
  (`--tell` / `--recall` / `--goal` / `--account`) exist in the copied
  file but Anna never passes them.
- **Anna-side code never edits engine files.** The engine is called
  as a subprocess and its output taken verbatim.

## Updating the copy

Re-copy the same file set from dc at the newer commit and change the
commit line above. If the two ever disagree, dc is the truth and this
folder is stale.

## Requirements

The engine needs only `numpy` for the faces Anna uses.
(`scikit-learn` in dc's requirements serves dc's demos and
experiments, which were not copied.)
