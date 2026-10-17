# 📚 End-to-End Scientific Paper Creation & Preprint Dissemination Guide: The BootcampGIS GeoAI Paper

**Lead Author & Principal Investigator:** Dr. Atilio Efrain Bica Grondona  
**Collaborative Methodology:** AI-Assisted Agentic Peer-to-Peer Pair Programming  
**Target Publication Standard:** Q1 Top-Tier (*IJGIS*, *CEUS*, *ISPRS*)  
**Dissemination Platform:** arXiv (`cs.AI` / `cs.MA` / `physics.geo-ph`)  
**Repository Tracked:** [bootcampgis-paper-private](https://github.com/atilioebg/bootcampgis-paper-private)  
**Date:** October 2026  

---

## Table of Contents
1. [Overview & Philosophy of Agentic Scientific Writing](#1-overview--philosophy-of-agentic-scientific-writing)
2. [Phase 1: Project Grounding & Research Questions](#2-phase-1-project-grounding--research-questions)
3. [Phase 2: Codebase Mining & Experimental Asset Pipeline](#3-phase-2-codebase-mining--experimental-asset-pipeline)
4. [Phase 3: LaTeX Engineering & Compilation Rigour](#4-phase-3-latex-engineering--compilation-rigour)
5. [Phase 4: Authorship, Front-Matter & Institutional Alignment](#5-phase-4-authorship-front-matter--institutional-alignment)
6. [Phase 5: Bibliography & arXiv Packaging (AutoTeX Preparation)](#6-phase-5-bibliography--arxiv-packaging-autotex-preparation)
7. [Phase 6: Navigating the arXiv Gate & Category Endorsements](#7-phase-6-navigating-the-arxiv-gate--category-endorsements)
8. [Summary Checklist for the BootcampGIS Manuscript](#8-summary-checklist-for-the-bootcampgis-manuscript)

---

## 1. Overview & Philosophy of Agentic Scientific Writing

This guide defines the exact operational methodology for converting the **BootcampGIS GeoAI Stack** into a publication-ready **Q1 journal manuscript** (*IJGIS* or *CEUS*) and an active **arXiv preprint**.

### The Core Principles:
* **Strict Zero-Hallucination Grounding:** Every baseline metric, iteration count, coordinate deviation, and execution latency must be extracted directly from verified execution runs on the local GeoStack.
* **The "Reviewer #2" Mindset:** Explicitly anticipate critiques regarding spatial data leakage, benchmark generalizability, and LLM non-determinism from the first draft.
* **Micro-Typographical Perfection:** Zero compilation warnings, zero bad box breaks, and column-width equation compliance.
* **Dual Dissemination:** Establish immediate scientific priority via arXiv, followed by peer-reviewed submission to an elite Q1 journal.

---

## 2. Phase 1: Project Grounding & Research Questions

Before drafting LaTeX, formalize the core narrative around the spatial AI reliability bottleneck:

1. **Define the Research Gap Explicitly:**
   * *Problem:* "While foundational LLMs exhibit sophisticated natural-language reasoning, their integration into geospatial decision-support systems introduces severe failure modes: geometric hallucination, dropped coordinate bounds, non-terminating retry loops, and inability to maintain spatial topological invariants."
2. **Articulate the Novel Contribution (The 'Why'):**
   * *Contribution:* "A self-healing Actor-Critic multi-agent swarm architecture governed by Pre-LLM Deterministic Geometric Sensors and Cognitive Blueprint schema caching, guaranteeing finite-step convergence ($K \le 3$) and zero geometric invariant violations across complex multi-facility logistics and geomarketing site selection."
3. **Select Publication Targets:**
   * **Primary Journal:** *International Journal of Geographical Information Science (IJGIS)* — Taylor & Francis (Q1, IF ~5.5).
   * **Alternative Journal:** *Computers, Environment and Urban Systems (CEUS)* — Elsevier (Q1, IF ~7.2).
   * **Preprint:** arXiv (Primary: `cs.AI`, Cross-lists: `cs.MA`, `physics.geo-ph`).

---

## 3. Phase 2: Codebase Mining & Experimental Asset Pipeline

The asset pipeline extracts quantitative empirical results directly from the repository:

1. **Extract Exact Metrics from Test & Benchmark Runners:**
   * Run the test suite: `pytest tests/unit/` and `pytest tests/integration/`.
   * Execute the `GeoSwarm-Bench` evaluation harness across all four ablation baselines (B1: Naive ReAct, B2: Pure LLM Actor-Critic, B3: Deterministic-Only, B4: Proposed Swarm).
   * Record exact quantitative metrics:
     * Execution Accuracy (EX %)
     * Geometric Invariant Violation Rate (GIVR %)
     * Prompt and completion token consumption per query
     * Time-to-convergence ($T_{	ext{conv}}$)
2. **Generate Publication-Grade Figures (300+ DPI):**
   * Save figures directly into `manuscript/figures/`:
     * **Figure 1:** End-to-end swarm topology flowchart (Planner $	o$ Worker $	o$ Sensor $	o$ Reviewer $	o$ Brake).
     * **Figure 2:** Multi-panel spatial layout: Road network centroid snapping, catchment buffer polygon, and POI distribution.
     * **Figure 3:** Iteration distribution and convergence rate bar charts comparing Baselines 1–4.
     * **Figure 4:** Folium web mapping interface demonstrating winner candidate placement.

---

## 4. Phase 3: LaTeX Engineering & Compilation Rigour

Formatting a two-column journal manuscript requires strict mathematical and typographical discipline:

### 4.1. Equation Margin Overflow (The 3.5-inch Rule)
In two-column layouts, single equations exceeding column width (~3.5 inches) collide with adjacent text:
* **Bad:** Unbroken single `egin{equation} ... \end{equation}`.
* **Fix:** Use `egin{equation}egin{aligned} ... \end{aligned}\end{equation}` with alignment markers (`&`) and explicit linebreaks (`\`).

### 4.2. Mathematical Notation & PDF Bookmarks
* Wrap mathematical symbols in section headings with `	exorpdfstring{$K \le 3$}{K <= 3}` to eliminate `hyperref` token warnings.
* Define custom hyphenations in the preamble: `\hyphenation{geo-spa-tial post-gis geo-mar-ket-ing}`.

---

## 5. Phase 4: Authorship, Front-Matter & Institutional Alignment

* **Lead Author & Principal Investigator:** Dr. Atilio Efrain Bica Grondona  
  *Affiliation:* Universidade Federal do Rio Grande do Sul (UFRGS) / BootcampGIS  
  *Email:* (Institutional address)  
  *Markings:* Corresponding Author ($^*$) with complete institutional footnote.
* **Running Headers:** Format as:  
  `\markboth{IEEE Transactions / IJGIS Draft}{Grondona: Self-Healing Actor-Critic Swarms for Spatial Optimization}`.

---

## 6. Phase 5: Bibliography & arXiv Packaging (AutoTeX Preparation)

arXiv compiles with `pdflatex` but **does not run BibTeX**:
1. Compile the manuscript locally or in Overleaf to produce `output.bbl`.
2. Rename `output.bbl` to `main.bbl` (matching `main.tex`).
3. Bundle `main.tex`, `main.bbl`, and `figures/` into a `.tar.gz` or `.zip` archive.
4. Verify that no absolute local paths or unused image files remain in the package.

---

## 7. Phase 6: Navigating the arXiv Gate & Category Endorsements

* **Primary Category:** `cs.AI` (Artificial Intelligence) or `cs.MA` (Multi-Agent Systems).
* **Cross-List:** `physics.geo-ph` (Geophysics).
* **Endorsement Code:** If submitting to `cs.AI` for the first time, obtain an endorsement code from an established academic author who has published $\ge 2$ papers in that category.

---

## 8. Summary Checklist for the BootcampGIS Manuscript

```markdown
- [ ] 1. BENCHMARK & ABLATION
      - [ ] Curate 150 benchmark spatial queries (GeoSwarm-Bench).
      - [ ] Run 4-way ablation (B1: Naive, B2: Pure LLM, B3: Deterministic, B4: Proposed).
      - [ ] Record EX (%), GIVR (%), Token Costs, and Latency.

- [ ] 2. FIGURE & TABLE ASSETS
      - [ ] Render 300+ DPI vector flowchart of the Actor-Critic Swarm.
      - [ ] Export spatial catchment and route maps directly to manuscript/figures/.
      - [ ] Format Table 1 (Ablation Benchmark Comparison).

- [ ] 3. LATEX ENGINEERING
      - [ ] Column width compliance for all spatial snapping and buffer equations.
      - [ ] Verify 0 Errors and 0 Warnings in LaTeX compilation.
      - [ ] Configure 	exorpdfstring in math section headings.

- [ ] 4. PREPRINT & SUBMISSION
      - [ ] Bundle main.tex, main.bbl, and figures into submission archive.
      - [ ] Deploy preprint to arXiv (cs.AI / cs.MA).
      - [ ] Submit manuscript to IJGIS (Taylor & Francis).
```

---
*This guide serves as the standard operating procedure for the BootcampGIS paper project.*
