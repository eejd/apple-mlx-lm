# Work carried on `local` that is not in ml-explore/mlx-lm

`local` = upstream release tag (v0.32.2 = `main` at the time of writing) + the `topic/*`
branches below, merged with `--no-ff`. `main` mirrors `ml-explore/mlx-lm` `main`
(fast-forward only). Each topic branch is one change on top of `main`.

| Topic branch | What | Upstream | Original branch (PR head, kept) |
|---|---|---|---|
| `topic/qwen3-coder-bare-function` | recover Qwen3-Coder tool calls written without the opening `<tool_call>` marker | not submitted (eejd/py-mlx-lm#3) | `fix/qwen3-coder-bare-function` |
| `topic/mistral-tool-parser-from-vocab` | infer the mistral tool parser from the `[TOOL_CALLS]` vocab token | ml-explore/mlx-lm#1969, closed (withdrawn 2026-10-16); eejd/py-mlx-lm#1 | `fix/mistral-tool-parser-from-vocab` |
| `topic/batch-kv-cache-fast-mask` | skip the attention mask in batch caches with no padding | ml-explore/mlx-lm#1970, closed (withdrawn 2026-10-16); eejd/py-mlx-lm#2 | `fix/batch-kv-cache-fast-mask` |

Not on `local` (not carried by any port): `fix/gpt-oss-harmony-channel-parsing`
(ml-explore/mlx-lm#1867, open; eejd/py-mlx-lm#4). Its branch is still the upstream PR's head.

The `fix/*` branches are the heads of the upstream PRs above and are left untouched; the
`topic/*` branches are their content rebased onto `main` (v0.32.2).
