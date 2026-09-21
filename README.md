# Mixley Synthesis Data Spec

The specification for the Synthesis Data network protocol.

## Status

**Specification - closed alpha.** The network runs in a closed alpha: operators can onboard nodes from the product while emission knobs and inference payouts are still calibrated. This repository tracks the protocol contributors implement in [mixley-node-worker](https://github.com/MixleyApp/mixley-node-worker) (private) and validate against the public docs.

## What the protocol is

The Synthesis Data network is a distributed and verified AI inference fabric. Nodes generate, re-execute, validate and cryptographically attest synthetic training data at scale. Accepted results enter cycle-specific canonical datasets.

## Files

- `spec/task-manifest.md` - the signed task manifest schema
- `spec/consensus.md` - consensus rules, the acceptance threshold, validator requirements
- `spec/reward-formula.md` - the reward components and formula
- `spec/states.md` - node and job states

The reference for this specification is the Synthesis Data network section of the [Mixley docs](https://mixley.app/docs).

## License

MIT - see [LICENSE](./LICENSE).
