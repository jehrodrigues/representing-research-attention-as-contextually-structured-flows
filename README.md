# Representing Research Attention as Contextually Structured Flows

Source code for the paper *Representing Research Attention as Contextually
Structured Flows*, accepted at the Science and Technology Indicators (STI)
Conference, 2026.

## Overview

Research metrics increasingly use attention as evidence of societal impact, but
altmetrics records signals in isolation, keeping only a count of how much
attention an output received or a sequence of when. We introduce the **attention
flow**, a representation that situates an output's attention in the contexts
through which it is distributed: the social settings where it occurs, the
language expressing it, and the time over which it unfolds.

We learn the flow with dynamic contextualised representations (/dcwe), yielding three
variants along two axes, contextual and dynamic:

- **CWE** — contextualised word embeddings (conditions on the linguistic context)
- **DWE** — dynamic word embeddings (conditions on the social context over time)
- **DCWE** — dynamic contextualised word embeddings (both)

To evaluate the flow, we build a benchmark of analogy queries (/data), each testing
whether the relationship between two outputs, applied to a third, yields a
fourth. We probe three structural properties of attention:

- **Invariance** — the structure is general across outputs
- **Preservation** — the structure is stable as attention develops
- **Dependence** — the structure rests on the contexts, not on volume alone

## Findings

The count and sequence baselines fail to recover the analogy relationships,
while the flow variants recover them. The recovered structure is general across
outputs, survives partial observation, and rests on the contexts rather than
volume. DCWE recovers this structure most fully.