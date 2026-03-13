# Work Log

`results.tsv` is the authoritative experiment ledger for this repository.

## Current Best

- Date: `2026-03-12`
- Commit: `234571e`
- `val_bpb`: `1.200930`
- Peak memory: `8.2 GB`
- Description: `tune weight decay to 0.06`

## Current Training Config

- `DEPTH = 6`
- `DEVICE_BATCH_SIZE = 16`
- `TOTAL_BATCH_SIZE = 2**15`
- `MATRIX_LR = 0.03`
- `WEIGHT_DECAY = 0.06`

## Notes

- Earlier entries in `results.tsv` have `time = unknown` where exact timestamps were not recorded at the time of the run.
- `work_log.md` is a lightweight summary only. Use `results.tsv` for experiment-by-experiment history.
