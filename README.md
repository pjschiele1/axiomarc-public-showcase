# AxiomARC Public Showcase

**Canonical-state infrastructure for reducing unnecessary computational work.**

[Interactive Hugging Face Showcase](https://huggingface.co/spaces/Pjschiele1/axiomarc-showcase) · [AxiomARC at OMporium](https://www.omporium.biz/axiomarc) · [Contact OMporium](https://www.omporium.biz/)

AxiomARC maintains canonical knowledge of computational state so a system can determine what already exists, what changed, what remains valid, and what actually needs to execute.

This repository is the technical companion to the public AxiomARC Hugging Face showcase. It documents architecture boundaries, evidence classes, benchmark methodology, and integration concepts without exposing proprietary implementation details.

## Mechanism overview

![AxiomARC — Not Less Information. Less Work.](https://huggingface.co/spaces/Pjschiele1/axiomarc-showcase/resolve/main/assets/not-less-information-less-work.png)

The public mechanism model is intentionally high level:

**Know the State → Constrain the Work → Reduce Realized Cost**

The implementation behind canonicalization, identity resolution, persistence, reconstruction, and policy behavior remains proprietary.

## Public evidence model

The public evidence package distinguishes:

- **MEASURED** — directly observed in the frozen validation workload.
- **DERIVED** — calculated from measured values or validated identity/lifecycle rules.
- **PROJECTED** — scaled scenario output; not a new physical run.
- **REFERENCE** — measured values carried from a separate controlled persistence/reconstruction reference cell.
- **NOT CLAIMED** — metrics the showcase deliberately does not infer.

## Measured anchor

The frozen public validation anchor contains:

- 300 logical requests
- 900 reference stage calls
- 480 AxiomARC-controlled stage calls
- 420 stage calls avoided
- 140 generation-engine calls avoided
- 126,480 of 224,400 reference pipeline work units avoided
- 300/300 outcome parity
- 0 unsafe reuse observed

See [Evidence and Claims](docs/evidence-and-claims.md) for scope and claim boundaries.

## Architecture boundary

AxiomARC is the canonical-state, identity, lineage, lifecycle, validity, persistence-intent, and reuse-control layer.

External systems remain responsible for retrieval, generation, evaluation, and other execution work.

See [Architecture Overview](docs/architecture-overview.md).

## Repository contents

- [Architecture Overview](docs/architecture-overview.md)
- [Evidence and Claims](docs/evidence-and-claims.md)
- [Benchmark Methodology](docs/benchmark-methodology.md)
- [Integration Overview](docs/integration-overview.md)
- [Machine-readable Evidence](evidence/evidence.json)
- [Public Repository Notice](NOTICE.md)

## Public-release boundary

This repository does **not** include AxiomARC production source code, proprietary canonicalization logic, identity algorithms, policy internals, persistence implementation, serving-engine implementation, or internal milestone archives.

## Contact

Interested in a pilot integration, infrastructure partnership, or technical discussion?

Visit **OMporium** at https://www.omporium.biz/
