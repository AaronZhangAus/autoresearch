# Work Log

## March 12, 2026

### Status

`train.py` now runs successfully without startup errors.

### Training Run 1

#### Notes

Initial successful training run.

#### Full Log

```text
Warning: failed to load Flash Attention kernel (Cannot install kernel from repo kernels-community/flash-attn3 (revision: main)). Falling back to PyTorch SDPA.
Warning: torch.compile disabled, using eager mode (Triton unavailable (No module named 'triton')).
Vocab size: 8,192
Model config: {'sequence_len': 2048, 'vocab_size': 8192, 'n_layer': 4, 'n_head': 2, 'n_kv_head': 2, 'n_embd': 256, 'window_pattern': 'L'}
Parameter counts:
  wte                     : 2,097,152
  value_embeds            : 4,194,304
  lm_head                 : 2,097,152
  transformer_matrices    : 3,145,856
  scalars                 : 8
  total                   : 11,534,472
Estimated FLOPs per token: 5.662387e+07
Scaling AdamW LRs by 1/sqrt(256/768) = 1.732051
Time budget: 300s
Gradient accumulation steps: 2
step 03481 (100.0%) | loss: 3.619899 | lrm: 0.00 | dt: 88ms | tok/sec: 185,705 | mfu: 1.1% | epoch: 1 | remaining: 0s
---
val_bpb:          1.283759
training_seconds: 300.0
total_seconds:    349.7
peak_vram_mb:     1626.6
mfu_percent:      1.09
total_tokens_M:   57.0
num_steps:        3482
num_params_M:     11.5
depth:            4
```

### Next Step

Kick off the smoke test and record the result below.

### Smoke Test Run

#### Notes

Recorded follow-up 5-minute run.

#### Full Log

```text
scalars                 : 8
total                   : 11,534,472
Estimated FLOPs per token: 5.662387e+07
Scaling AdamW LRs by 1/sqrt(256/768) = 1.732051
Time budget: 300s
Gradient accumulation steps: 2
step 03457 (100.0%) | loss: 3.568453 | lrm: 0.00 | dt: 90ms | tok/sec: 181,595 | mfu: 1.0% | epoch: 1 | remaining: 0s
---
val_bpb:          1.287775
training_seconds: 300.0
total_seconds:    351.6
peak_vram_mb:     1626.6
mfu_percent:      1.08
total_tokens_M:   56.7
num_steps:        3458
num_params_M:     11.5
depth:            4
```
