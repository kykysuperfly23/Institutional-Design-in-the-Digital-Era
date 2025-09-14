# Bargaining by "Dividing-the-Dollar": An Interdisciplinary Study

## Abstract
We study a two-player bargaining (Nash demand) game across three lenses: **economist** (theory & welfare), **computational scientist** (algorithmic computation and extensive-form modeling), and **behavioral scientist** (human vs. LLM play in repeated rounds). The normal form exhibits **frontier multiplicity** and frequent **degeneracy** in solver outputs, while a GTE (Game Theory Explorer) tree with a single information set reproduces simultaneous-move equilibria as SPNE. In brief experiments, humans showed sharp “post-bust” caution, whereas LLMs adjusted smoothly toward fair splits with payoff visibility. We propose a simple refinement—bust-salient, aspiration-based choice—as a bridge between predictions and observed behavior.

---

## Task Summary
- **Part 1 — Economist (theory & welfare):**  
  Formalize the bargaining problem \((F,d)\); present the **Nash Bargaining Solution** and **Kalai–Smorodinsky** refinement; connect cooperative benchmarks to the simultaneous **divide-the-dollar** game and discuss multiplicity, bounded rationality, and tractability.  
  _See:_ `economist/README.md` and `economist/refs/`.

- **Part 2 — Computational Scientist (coding & tools):**  
  **2a.** Build normal-form payoff matrices and compute equilibria with **NashPy** (include solver outputs and matrices).  
  **2b.** In **GTE**, build the extensive form with P2’s nodes in one information set (simultaneity), solve with SPNE, and capture screenshots of the tree and solution panel.  
  _See:_ `computational_scientist/README.md`, `computational_scientist/notebook.ipynb`, `computational_scientist/screenshots/`, and optional `computational_scientist/gte/`.

- **Part 3 — Behavioral Scientist (experiment & AI comparison):**  
  **3a.** Deploy an **oTree** app (5-round repeated play), run a short human session, and save screenshots.  
  **3b.** Run an **LLM vs LLM** session (ChatGPT vs Claude) with identical framing; log prompts, settings, and transcripts.  
  **3c.** Provide a concise comparative analysis (humans vs LLMs vs theory).  
  _See:_ `behavioral_scientist/README.md`, `behavioral_scientist/otree_app.zip`, `behavioral_scientist/screenshots/`, and `behavioral_scientist/llm/`.

---

## Reproduction Steps

### 0) Clone and prepare
```bash
git clone <this-repo-url>
cd <repo-root>
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate
