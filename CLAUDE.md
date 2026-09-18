
# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is the LaTeX manuscript source for a Master's paper (NUST, Department of Software Engineering) describing **`jnang`** — the Ju|'hoansi Narrative Agentic Generator, an ontologically grounded multi-agent system for generating culturally authentic Ju|'hoansi (Khoisan) folktales. The paper argues that off-the-shelf LLMs and Proppian narrative formalisms inject Western/Indo-European tropes into indigenous oral traditions, and proposes a fix combining an RDF/OWL narrative ontology, a Neo4j knowledge graph, and a 3-agent LangGraph pipeline (Generator → Classifier → Evaluator).

**This repo contains only the manuscript, not the `jnang` implementation.** The actual code (agents, RDF ontology, Neo4j import scripts, 3D graph visualizer) lives in a separate sibling repository (`jnang`). `.agents/references/jnang_documentation.md` is a detailed technical dossier on that external system — use it to understand *what the paper is describing* and to keep terminology/file names in the manuscript consistent with the real implementation, but do not expect that code to be present here.

## Compiling the paper

Single-file Springer Nature journal article, class option `sn-mathphys-num` (numbered references, math/physical sciences style):

```
pdflatex sn-article.tex
bibtex sn-article
pdflatex sn-article.tex
pdflatex sn-article.tex
```

Two `pdflatex` passes after `bibtex` are required to resolve citations and the reference list. The `.bst` files other than `sn-mathphys-num.bst` (apacite, aps, basic, chicago, nature, vancouver-*) belong to the template and are unused unless the `\documentclass` option in `sn-article.tex` is changed.

There is no Makefile or latexmkrc — run the four commands above directly, or use `latexmk -pdf sn-article.tex` if available.

## File map

- `sn-article.tex` — the entire manuscript (title/abstract through Declarations). All section content lives in this one file; there are no `\input`/`\include` sub-files.
- `sn-bibliography.bib` — BibTeX source, cited via `\cite{}` keys matching entries here (e.g. `biesele2006ju`, `dundes1964morphology`, `Adelani2022`).
- `sn-jnl.cls`, `sn-*.bst` — vendored Springer Nature template files. Do not edit unless fixing a template-level bug; content changes belong in `sn-article.tex` / `sn-bibliography.bib`.
- `fig.eps`, `empty.eps` — figure assets referenced via `\includegraphics`.
- `sn-article.pdf`, `sn-article.html`, `user-manual.pdf` — build outputs / template documentation, not edited by hand.
- `SOURCE_OF_TRUTH.md` — the writing plan for this paper: narrative philosophy, 12-page budget allocation per section, the 5-step introduction pitch arc, citation strategy (which sources are already integrated vs. reserved for later), and a phase-by-phase progress checklist. **Read this before drafting or restructuring any section** — it records author decisions already made and what's still pending.

## Writing workflow conventions

These come from `SOURCE_OF_TRUTH.md` §1 ("Working Rules & Collaboration Protocol") and govern how edits to `sn-article.tex` should be made:

1. **Preserve author authority** — don't overwrite prose the author has already written or revised. Ask before making major structural changes; grammar/flow polish that preserves exact technical and cultural meaning can be done directly.
2. **Work section-by-section**, tracking progress against the checklist in `SOURCE_OF_TRUTH.md` §5 rather than jumping between sections.
3. Keep the **Ju|'hoansi people and their oral tradition as the subject of the story**, not just the tool — this framing is the paper's core philosophy (`SOURCE_OF_TRUTH.md` §0).
4. Preserve exact terminology tied to the ontology and system design (motifemes, Camp/Bush spatial axis, oicotypes, agent names) — these map 1:1 to concepts in the external `jnang` codebase and must stay consistent with `.agents/references/jnang_documentation.md`.

## Available skills for this repo

- `research-paper-writing` (`.agents/skills/research-paper-writing/`) — section-specific guidance (introduction, abstract, related work, method, experiments, conclusion) and an adversarial self-review checklist. Load only the reference file for the section actually being edited, not all of them at once.
- `stop-slop` (`.agents/skills/stop-slop/`) — checklist for removing AI-writing tells (filler phrases, passive voice, formulaic contrasts) before finalizing prose.
