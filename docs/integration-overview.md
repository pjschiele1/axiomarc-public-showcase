# Integration Overview

## Where AxiomARC fits

AxiomARC is designed to sit between application/workflow state and specialized execution systems.

The integration question is not “Which engine does AxiomARC replace?”

It is:

**Can the system determine what state already exists, what changed, what remains valid, and which execution work is actually required?**

## Representative workflow

A public conceptual workflow is:

**Request → Identity / lifecycle resolution → Reuse / restore / execute decision → External execution system → Updated canonical state**

AxiomARC supplies the canonical-state and lifecycle context.

External systems continue to perform execution.

## Representative integration points

Potential integration surfaces include:

### Retrieval

A retrieval system can remain the execution owner while AxiomARC tracks retrieval identity, authoritative source/version context, lineage, and reuse validity.

### Generation

A model-serving engine remains responsible for generation. AxiomARC can determine whether an exact/current generation state is reusable or whether fresh execution is required.

### Evaluation

An evaluator remains responsible for scoring or validation. AxiomARC can track independent evaluation identity, evaluator/rubric version, lineage, and validity.

### Persistence and recovery

AxiomARC can manage canonical persistence intent and restore lifecycle while execution-ready state remains owned by the external serving engine.

## Change propagation

Representative public scenarios include:

- source identity changes
- model identity changes
- generation-configuration changes
- evaluator identity changes
- rubric or policy identity changes

The public showcase demonstrates how different changes can invalidate different portions of the reusable state graph.

The underlying identity and policy algorithms are proprietary and are not included here.

## Deployment model

The public materials describe AxiomARC as infrastructure that integrates with existing tools and environments rather than requiring customers to replace their execution stack.

Pilot discussions can focus on:

- workload definition
- identity boundaries
- authoritative state transitions
- correctness gates
- measurable work avoided
- persistence/reconstruction behavior
- resource and economic accounting

## Contact

For pilot integration, infrastructure partnerships, or technical evaluation, visit:

https://www.omporium.biz/
