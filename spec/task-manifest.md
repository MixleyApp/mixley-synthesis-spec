# Task Manifest

A task in the Synthesis Data network is described by a signed task manifest. The manifest is issued by the control plane and selected by the scheduler for eligible nodes.

## Schema

| Field | Type | Purpose |
| --- | --- | --- |
| `task_id` | string | Stable identifier for this task |
| `cycle` | string | The cycle this task belongs to, e.g. `synth-v1` |
| `model_alias` | string | The model alias the task targets |
| `model_version` | string | The immutable deployment version of the model |
| `input_hash` | string | Hash of the task input |
| `output_size_limit` | integer | Maximum accepted output size |
| `comparison` | enum | `exact`, `deterministic_hash`, `semantic`, `constraint`, `quality` |
| `signature` | string | Control-plane signature over the manifest |

## Comparison modes

A generative task cannot always rely on byte-for-byte equality, so each task declares which comparison is valid:

- **exact** — byte-for-byte output equality
- **deterministic_hash** — equality of a deterministic hash of the output
- **semantic** — semantic similarity above a threshold
- **constraint** — a set of constraints the output must satisfy
- **quality** — a model-specific quality check

## Signature

The manifest is signed by the control plane. The signature binds the task to a cycle, a model alias and an immutable model version, so a node cannot substitute a different model and claim the result for this task.
