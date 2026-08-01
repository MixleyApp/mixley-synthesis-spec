# Consensus

Peer verification reduces dependence on a single operator. Policy may compare exact outputs, deterministic hashes, semantic similarity, constraint satisfaction or model-specific quality checks.

## Acceptance

A result is accepted when the fraction of agreeing validators meets the consensus threshold:

```
accept if
  agreeing_validators
  ─────────────────────
  total_validators
        ≥ consensus_threshold
```

## Examples

| Validators | Agreeing | Fraction | Threshold | Outcome |
| --- | --- | --- | --- | --- |
| 5 | 4 | 0.80 | 0.75 | accepted |
| 5 | 3 | 0.60 | 0.75 | escalated |

## Additional requirements

Consensus may additionally require:

- A minimum number of independent validators
- Hardware, geographic or operator diversity
- A confidence threshold
- No critical policy violation
- Valid task and model-version attestations

## Escalation

A result that does not meet the threshold is escalated, not discarded. Escalation triggers a wider review or a different comparison policy.
