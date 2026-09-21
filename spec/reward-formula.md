# Node Reward

A node is rewarded for accepted work, not for registration. Eligibility follows accepted work, so the size of the allocation does not by itself determine what an individual operator receives.

MIX payouts for verified node work settle on **Robinhood Chain** once emission is enabled. Until then, the dashboard may show accrued points without an on-chain transfer. Block 0 bootstrap and ongoing tax or buyback-funded rewards are product configuration, not constants in this document.

## Formula

```
node_reward = uptime_component
              + accepted_validation_component
              + accepted_inference_component
```

## Worked example

| Component | Calculation | Result |
| --- | --- | --- |
| Uptime 98% of the window, weight 50 | 0.98 × 50 | 49.0 |
| 1,240 accepted validations at 0.05 | 1,240 × 0.05 | 62.0 |
| 310 verified compute units at 0.40 | 310 × 0.40 | 124.0 |
| **Total for the cycle** | 49.0 + 62.0 + 124.0 | **235.0** |

## Quality factors

Each component may be multiplied by quality, reputation, demand or scarcity factors. Rejected, duplicated, late or fraudulent work receives no normal reward credit, and any penalty or slashing policy must be disclosed before activation.
