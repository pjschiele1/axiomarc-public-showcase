# Architecture Overview

## Purpose

AxiomARC is canonical-state infrastructure designed to help a system determine what computational state already exists, what changed, what remains valid, and what work actually needs to execute.

The public architecture is intentionally described at the system-boundary level. This repository does not disclose proprietary canonicalization, identity, persistence, reconstruction, or policy implementation.

## Core role

AxiomARC provides the state-control layer around existing execution systems.

Its public responsibilities are described as:

- canonical state
- identity
- lineage
- lifecycle
- validity
- persistence intent
- reuse control

Execution systems remain responsible for performing fresh work when AxiomARC determines that execution is required.

## Execution boundary

Representative external systems may include:

- retrieval engines
- model-serving engines
- evaluators
- data-processing systems
- training or fine-tuning systems
- agent runtimes

AxiomARC does not replace those engines. It determines whether known state remains valid and reusable, whether state must be restored or reconstructed, or whether fresh execution is required.

## Public mechanism model

The public showcase explains the mechanism as:

**State Capacity → State Sparsity → Canonical State Resolution → Expected Work → Resource Cost**

A complementary operational view is:

**Know the State → Constrain the Work → Reduce Realized Cost**

These phrases describe the observable system role, not the proprietary implementation.

## Important distinctions

### Compression

Compression represents equivalent information using fewer bits.

### State sparsity

Only a subset of possible states or transitions is realized or relevant to a particular workload.

### Work reduction

Fewer operations or states need to be evaluated to reach the required result.

### Resource reduction

Less execution, memory activity, data movement, I/O, and potentially energy may be required when unnecessary work is avoided.

AxiomARC should not be interpreted as claiming that canonical state mathematically reduces the full state space or that logical state-footprint reduction is identical to physical VRAM release.

## Persistence and execution state

The public lifecycle distinguishes:

**KEEP → PERSIST → RESTORE → RE-PRIME**

The serving engine remains the owner of active execution-ready state.

AxiomARC persistence refers to a compact canonical representation rather than automatically persisting active exact-KV state as the canonical object.

## Scope

This document describes public architecture boundaries only. It intentionally omits internal algorithms, data structures, source code, milestone artifacts, and implementation-specific control logic.
