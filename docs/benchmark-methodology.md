# Benchmark Methodology

## Objective

The public benchmark package demonstrates how AxiomARC-controlled execution can avoid unnecessary pipeline work while preserving the validated outcome of the reference workflow.

The public package is evidence-focused and does not expose production implementation details.

## Integrated anchor

The measured public anchor contains 300 logical requests passing through a three-stage reference workflow:

1. knowledge retrieval
2. generation
3. evaluation

A conventional reference path executes all three stages for every request:

- 300 retrieval calls
- 300 generation calls
- 300 evaluation calls
- 900 total stage calls

The AxiomARC-controlled measured path executes:

- 120 retrieval calls
- 160 generation calls
- 200 evaluation calls
- 480 total stage calls

Observed difference:

- 420 stage calls avoided

## Correctness boundary

The measured anchor records:

- 300/300 outcome parity
- 0 unsafe reuse observed

The public showcase does not treat avoided calls as sufficient evidence of correctness by themselves. Reuse is only counted when the validated canonical state satisfies the identity/lifecycle rules used by the controlled workload.

## Work accounting

Reference Pipeline Work is used as a deterministic accounting measure for the processing associated with retrieval/source exposure, generation, and evaluation.

Measured anchor:

- reference: 224,400 units
- controlled: 97,920 units
- avoided: 126,480 units
- reduction: 56.36%

Reference Pipeline Work is not automatically equivalent to:

- provider-billed tokens
- GPU seconds
- GPU joules
- dollars

## Scenario model

The public interactive showcase includes larger/smaller workload volumes and identity-change scenarios.

Those outputs are labeled **PROJECTED** and/or **DERIVED** unless they reproduce the measured 300-request anchor.

They are not presented as new physical benchmark runs.

## Persistence reference

Persistence, restore, re-prime, storage-density, and re-prime-energy values come from a separate controlled reference cell.

They are classified as **REFERENCE** rather than merged into the measured 300-request integrated anchor.

## Reproducibility boundary

This repository provides public methodology, evidence values, and claim boundaries.

It does not include the proprietary AxiomARC production runtime, internal algorithms, or source code needed to recreate the product implementation.
