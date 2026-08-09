# Paper Source of Truth: Ju/|'hoansi Agentic Narrative Generation

> **Core Philosophy**: When writing this paper, we are essentially telling a story. This story puts the **Ju/|'hoansi people in the forefront** and demonstrates how the tool we built is directly useful to them for cultural preservation, structural fidelity, and respectful representation.

---

## 1. Writing Principles & Cascade Architecture

### Structural Hierarchy (Expansion Cascade)
- **Abstract** $\rightarrow$ Compressed kernel of the paper.
- **Introduction** $\rightarrow$ Expands the **Abstract** and establishes the core **Problem Statement**.
- **Problem Statement** $\rightarrow$ Expands and anchors the **rest of the paper** (Objectives, Related Work, Methods, Results, Discussion, Conclusion).

### Working Rules & Collaboration Protocol
1. **Preservation of User Authority**: Do not overwrite work that has been written or revised by the author. Query flow, request clarification, and suggest enhancements before making major changes.
2. **Grammar & Prose Polish**: Grammar, syntax, and flow enhancements may be polished directly while preserving exact technical and cultural meaning.
3. **Phased Section Execution**: Work systematically section-by-section.
4. **Progress Tracker**: Maintain a strict checklist of approved sections before moving to subsequent sections.

---

## 2. Page Budget Allocation (12-Page Limit Target)

| Page Target | Content Allocation | Key Focus |
| :--- | :--- | :--- |
| **Page 1** | Introduction, Background, Problem Statement, Objectives | Problem pitch, consequences, solutions, teasers |
| **Page 2** | Literature Review / Related Work | Biesele, Propp, Dundes, Finlayson |
| **Page 3–4** | Methods (Part 1: Data & Ontology) | Corpus collection, structural decomposition, ontology design |
| **Page 5–6** | Methods (Part 2: Agentic Architecture) | Agent mechanics, multi-agent workflows, graph retrieval |
| **Page 7–8** | Visuals, Diagrams & Sample Narrative | Architecture diagrams, prompt pipelines, sample generated stories |
| **Page 9–10** | Results & Metrics | Graphs of performance, 3-dimensional evaluation scoring |
| **Page 11** | Discussion & Conclusion | Translation integration (low-resource African MT), shortcomings |
| **Page 12** | References & Appendices | Comprehensive bib entries & declarations |

---

## 3. Detailed Section Breakdown & Narrative Setup

### 3.1 Introduction (5-Step Pitch Arc)
1. **Problem Pitch**: Off-the-shelf Large Language Models (LLMs) fail to produce structurally accurate Ju/|'hoansi narratives due to training bias on Western/Indo-European corpora.
2. **Big Numbers & Consequences**: Unconstrained LLMs inject Indo-European tropes (monarchs, gold coins, individual wealth accumulation $W^*$, punitive executions) into Khoisan oral traditions, erasing communal socio-ecological values.
3. **Current Solutions & Limitations**: Standard Retrieval-Augmented Generation (RAG) using raw Ju/|'hoansi text collections lacks explicit structural and cultural guardrails.
4. **Proposed Solution**: Graph RAG combined with an RDF Turtle Narrative Ontology grounded in Alan Dundes' 8 motifemes, Lévi-Straussian spatial axes (Camp vs. Bush), and explicit story moves.
5. **Results Teaser**: Brief preview of experimental findings showing 100% compliance on non-hoarding constraints and high cultural authenticity.

### 3.2 Problem Statement & Objectives (Adopted from Proposal)
- **Source Proposal Location**: [`4introduction.tex`](file:///C:/Users/lmy/source/repos/Master-Thesis-Lemuel-Mayinoti/sections/4introduction.tex)
- **Problem Statement**:
  > Language models and LLMs are currently the most effective tool for natural language generation and storytelling. However, they remain largely disconnected from Indigenous African languages such as Ju/'hoansi. Because these models have had little to no exposure to Khoisan languages and lack annotated digital corpora, they struggle to capture the socio-ecological frameworks, values, and storytelling traditions central to San communities. Unconstrained LLMs inject Western/Indo-European tropes (monarchs, gold coins, individual wealth accumulators $W^*$, and punitive executions) into folklore, eroding indigenous cultural heritage. This research tackles the challenge of using NLP and multi-agent systems to generate narratives that are both culturally meaningful and structurally faithful to low-resource indigenous languages like Ju/'hoansi.

- **Main Objective**:
  > To model, engineer, and evaluate an ontologically grounded multi-agent narrative generator (`jnang`) and integrated pipeline to create culturally authentic, structurally sound stories from existing Ju/'hoansi San oral traditions.

- **Sub-Objectives**:
  1. *Ontological Formalization*: Formalize Ju/'hoansi narrative mechanics (Dundes 8 motifemes, Lévi-Straussian Camp vs. Bush spatial dynamics, kinship networks, non-hoarding ethics) into an RDF Turtle ontology and Neo4j Knowledge Graph.
  2. *Agentic Fine-Tuning & Steering*: Develop a 3-agent orchestration system (Generator, Classifier, Evaluator) that guides LLM output to eliminate Western tropes.
  3. *Evaluation & Benchmarking*: Benchmark AI-generated stories against original Ju/'hoansi folktales on metrics of cultural authenticity, motifeme coherence, anti-hoarding adherence, and orthographic precision.
  4. *Translation Adaptation*: Integrate the framework into pre-translation structural adaptation layers for low-resource African Machine Translation (MT).

---

## 4. Citation Management & Bibliography Strategy

### Proposal Citation Pool (Preserved from `mybib.bib`)
We preserve and track all foundational citations from the proposal (`C:\Users\lmy\source\repos\Master-Thesis-Lemuel-Mayinoti\bib\mybib.bib`):
- **Ju/'hoansi Ethnography & Preservation**: Biesele (2006) `biesele2006ju`, Wiessner (2014) `wiessner2014`, Keeney & Keeney (2013) `keeney2013reentry`, Jones (2018) `jones2018will`.
- **Indigenous Co-Design & Resilience**: Kays, Goagoses & Winschiers-Theophilus (2023) `Kays2023`, Foelske et al. (2014) `foelske2014digital`.
- **African NLP & Machine Translation**: Adelani et al. (2022) `Adelani2022`, Lô et al. (2020) `Lo`.
- **NLP & LLM State-of-the-Art**: Khurana et al. (2023) `Khurana2023`, Sawicki et al. (2023) `Sawicki2023`, Naveed et al. (2023) `naveed2023comprehensive`.

### Target Citations to Strengthen the Manuscript
We explicitly reserve space for additional key references to elevate academic rigor:
- **Narrative Morphology & Formalism**: Vladimir Propp (1928) *Morphology of the Folktale*, Alan Dundes (1964) *The Morphology of North American Indian Folktales*, Claude Lévi-Strauss (1955) *The Structural Study of Myth*.
- **Computational Narrative Systems**: Mark Alan Finlayson (2012, 2017) on narrative structure learning and Annotation of Narrative Structure in Text (Analogical Storytelling / Story Workbench).
- **Knowledge Graphs & Multi-Agent Frameworks**: RDF/OWL W3C Standards, Neo4j Graph Databases in RAG (GraphRAG), LangGraph multi-agent orchestration paradigms.

---

## 5. Master Progress Checklist

- [x] **Phase 1**: Source of Truth Alignment & Architectural Decisions Confirmed via Interview
- [x] **Phase 2**: Proposal Problem Statement, Objectives & Bibliography Strategy Integrated
- [x] **Phase 3**: Introduction & Background Drafting (Page 1)
- [x] **Phase 4**: Literature Review / Related Work (Biesele, Propp/Dundes, Finlayson) (Page 2)
- [ ] **Phase 5**: Methods - Story Collection, Decomposition & Ontology (Pages 3–4)
- [ ] **Phase 6**: Methods - Agent Architecture & Workflow Diagrams (Pages 5–6)
- [ ] **Phase 7**: Visuals, Diagrams & Sample Narrative Abstract (Pages 7–8)
- [ ] **Phase 8**: Results, Performance Graphs & 3-D Grading (Pages 9–10)
- [ ] **Phase 9**: Discussion (Translation Integration & Shortcomings) & Conclusion (Page 11)
- [ ] **Phase 10**: Final 12-Page Polish & Reference Audit (Page 12)
