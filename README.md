# Flowmetrics: AI-Driven Modelling of Societal Research Impact

## Core Aim and Research Questions

**What**  
This research investigates whether societal research impact unfolds in a structured, progressive, and semantically meaningful manner across distinct dimensions. It introduces **Flowmetrics** as a conceptual model to represent these trajectories.

**Why**  
Current approaches to research impact assessment often rely on **static or fragmented metrics** such as citation counts, altmetric scores, or isolated platform mentions. These metrics fail to capture how impact emerges, accumulates, and flows across audiences and media over time. They also overlook the temporal structure and semantic progression of impact, limiting their ability to support nuanced, generalisable, and context-aware evaluation. A structured, temporally aware model can address these gaps by tracing how research disseminates and influences society in meaningful ways.

**How**  
Flowmetrics is operationalised through a sequence of three core contributions:  
(i) it is **empirically validated** by analysing the alignment between real-world dissemination patterns and a stage-based model of impact  
(ii) it is **formally modelled** using graph-based representations that structure relationships between research topics, platforms, and stages  
(iii) it is **computationally operationalised** through a neurosymbolic framework that combines structured reasoning with language model inference to predict and explain impact trajectories

### Research Questions

1. **RQ1.** To what extent does societal research impact unfold in a structured and progressive manner across different platforms and audiences?  
2. **RQ2.** How can platform-specific signals and topic relationships be modelled as structured, interpretable representations of research impact flows?  
3. **RQ3.** Can large language models, when guided by structured knowledge, reliably predict and explain plausible trajectories of societal impact for research topics?

The thesis is structured as four interlinked articles, each of which contributes a distinct and essential layer to the development of the Flowmetrics framework:

---

### [Article 0: *Traditional Research Metrics – A Historical Review*](https://www.overleaf.com/1853281758xwnhwjspvrmt#99c14a)

This foundational article traces the historical evolution of research metrics to contextualise the Flowmetrics framework. It examines the shift from citation-based to attention-based indicators and explores emerging AI-driven approaches.

**Contents Overview:**
- What constitutes research impact?  
- The evolution of research metrics  
  - Bibliometrics  
  - Scientometrics  
  - Webometrics  
  - Altmetrics  
- Beyond traditional metrics  
  - ML-based methods for estimating impact  
  - LLM-based methods for estimating impact

---

### Article I: *Mapping Research Impact – A Multidimensional Approach*

This article investigates how research dissemination unfolds across online platforms over time. It uncovers latent dissemination structures to support a stage-wise model of impact.

**Research Questions:**
- **RQ1.** What temporal patterns characterise the dissemination of research across online platforms?
- **RQ2.** How do platforms align with distinct stages in the research impact lifecycle?
- **RQ3.** Can platform activity empirically support a stage-based, multidimensional model of impact?

---

### Article II: *Modelling Research Impact – Nodes of Topics, Edges of Impact*

This article formalises dissemination patterns as structured graph representations, connecting research topics through shared or sequential impact flows.

**Research Questions:**
- **RQ1.** How can research topics be connected through shared or sequential patterns of impact across platforms?
- **RQ2.** What structural representations best capture the multidimensional relationships between research outputs, platforms, and impact stages?
- **RQ3.** How can graph-based representations of impact trajectories support downstream reasoning and prediction?

---

### [Article III: *Predicting Research Impact – A Neurosymbolic Approach Using LLMs and Knowledge Graphs*](https://www.overleaf.com/5458631815hprhthhdfzdt#c742c5)

This article explores how large language models (LLMs), augmented with structured knowledge, can predict and explain research impact trajectories.

**Research Questions:**
- **RQ1.** Can LLMs reliably infer impact stages between research topics from structured evidence?
- **RQ2.** To what extent do LLMs produce coherent and canonically ordered impact trajectories?
- **RQ3.** How consistent are impact stage predictions across different LLM families?

---

Together, these four articles trace a progression from conceptual foundations to empirical observation, symbolic modelling, and predictive reasoning, laying the groundwork for a new generation of temporally aware, semantically rich approaches to research impact assessment.

📄 [**Thesis Overleaf**](https://www.overleaf.com/6338262171tpwfdscyrjrw#4cdd28)

### Key Thesis Milestones

| Milestone                                              | Target Date       |
|--------------------------------------------------------|-------------------|
| Make ToS draft available for supervisor review         | 01 September 2025 |
| Submit online application to Transfer Status           | 15 October 2025   |
| Upload ToS document to GRS portal                      | 25 November 2025  |
| Milestone Interview                                    | January 2026      |
| Transfer of Status (ToS) completion deadline           | 25 April 2026     |

---

## Repository Structure

```bash
predicting-multidimensional-research-impact/
├── data/
│   └── impact_augmented_kg.ttl              # Serialized KG with platform scores and concept links
│   └── model.ttl                            # Semantic model
│   └── flowmetrics-predictions.csv          # Output from classification stage
├── experiments/
│   ├── Flowmetrics-foundation-data.ipynb        # (01) Implements a data collection pipeline for foundational experiments
│   ├── Flowmetrics-foundation.ipynb             # (01) Implements a suite of foundational experiments
│   ├── Flowmetrics-KG-construction.ipynb        # (03) Builds the impact-augmented knowledge graph (RDF/Turtle)
│   ├── Flowmetrics-LLM-classification.ipynb     # (03) Applies LLMs to predict impact stages for each topic pair
│   ├── Flowmetrics-validation.ipynb             # (03) Evaluates stage-level and sequence-level predictions
│   ├── config.py
│   └── utils.py
├── requirements.txt
└── README.md
```


## Installation

We recommend using a virtual environment to avoid dependency conflicts:

```bash
# Create and activate a virtual environment with Python 3.8
$ virtualenv venv -p python3.8
$ source venv/bin/activate

# Install dependencies
$ pip install -r requirements.txt
