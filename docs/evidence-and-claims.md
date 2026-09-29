# Evidence and Claims

AxiomARC public materials separate evidence by authority class so measured observations are not mixed with derived scenarios or projections.

## Evidence classes

| Class | Meaning |
|---|---|
| **MEASURED** | Directly observed in the frozen validation workload. |
| **DERIVED** | Calculated from measured values or validated identity/lifecycle rules. |
| **PROJECTED** | Scaled scenario output; not a new physical run. |
| **REFERENCE** | Measured value carried from a separate controlled persistence/reconstruction reference cell. |
| **NOT CLAIMED** | A metric the public showcase deliberately does not infer. |

## Measured public anchor

The frozen integrated validation anchor uses 300 logical requests.

| Metric | Reference | AxiomARC-controlled | Observed difference |
|---|---:|---:|---:|
| Stage calls | 900 | 480 | 420 avoided |
| Reference Pipeline Work | 224,400 | 97,920 | 126,480 avoided (56.36%) |
| Outcome parity | 300 requests | 300 matched | 300/300 |
| Unsafe reuse | — | 0 | 0 observed |

Additional measured-anchor execution counts:

- retrieval calls: 120
- generation calls: 160
- evaluation calls: 200
- generation-engine calls avoided: 140
- generation token work avoided: 12,880
- evaluation token work avoided: 5,600
- retrieval/source work avoided: 108,000

## Reference Pipeline Work

Reference Pipeline Work is a deterministic validation accounting unit used to compare controlled processing across retrieval/source exposure, generation, and evaluation.

It is **not automatically equivalent to** provider-billed tokens, GPU time, joules, or dollars.

## Persistence reference

A separate controlled persistence/reconstruction reference cell records:

- logical reusable exact-KV reference: 14.0 MiB
- durable canonical representation: 3,339 bytes
- representation density: 4,396.55×
- representation reduction: 99.9773%
- persist write: 99.087 ms
- restore read: 14.837 ms
- exact re-prime: 37.342 ms
- exact re-prime GPU energy: 1.8683 J
- restore + re-prime: 52.179 ms

These values are reference measurements from a separate controlled cell and should not be presented as measurements from the 300-request integrated anchor.

## Controlled source-recurrence characterization

These profiles characterize controlled source-state recurrence and are **not** typical-customer population estimates.

| Profile | Repeated exposure | Actually eliminated |
|---|---:|---:|
| High | 75.74% | 70.09% |
| Moderate | 46.37% | 37.17% |
| Low | 16.90% | 14.99% |

## Explicit non-claims

The public showcase does not claim that:

- logical reusable exact-KV footprint equals physical VRAM returned to the allocator;
- GPU seconds or joules saved can be inferred from generation-call avoidance alone;
- the public Space is a new live retrieval/generation/evaluation benchmark run;
- projected workload volumes are new physical measurements;
- controlled source-recurrence profiles represent a typical customer population;
- the public showcase contains or exposes the proprietary production AxiomARC runtime.

## Authority

The machine-readable public evidence file is available at [evidence/evidence.json](../evidence/evidence.json).
