# Economist — README (Part 1)

This folder contains the **theory & welfare** materials for Part 1 of the project.

## What this section does (short)
We formalize a **two-player bargaining problem** \((F,d)\), state the **Nash Bargaining Solution (NBS)** and an alternative refinement (**Kalai–Smorodinsky, KS**), and connect these to the **divide-the-dollar** normal form used later. We also give brief notes on **realism/multiplicity**, **bounded rationality**, and **computational tractability**.

## Citations with page/section pointers
Below are the sources you should cite **exactly where the concepts appear** in your write-up. Page ranges refer to the original journals; section cues help locate the relevant statements.

### Equilibrium concept (definition, axioms, existence/uniqueness)
- **Nash (1950)** *Econometrica* 18(2): **155–162** — defines the bargaining problem and the NBS; axioms (Pareto, symmetry, scale invariance, IIA) and uniqueness/existence argument appear across the paper (see esp. the middle sections).  
  *Use for:* formal definition of \((F,d)\), the NBS argmax \(\max_{x\in F, x\ge d}(x_1-d_1)(x_2-d_2)\), and the axiom list.
- **Nash (1953)** *Econometrica* 21(1): **128–140** — complementary cooperative-game framing.  
  *Use for:* background sentence on cooperative foundations.
- **Niederle (slides)** — *Nash Bargaining* (section titled “Nash product / geometry”).  
  *Use for:* the plain-language geometric line (“hyperbola tangent to frontier”).

### Alternative refinement (KS)
- **Kalai & Smorodinsky (1975)** *Econometrica* 43(3): **513–518** — KS solution; monotonicity instead of IIA; point on the line from \(d\) to the utopia point \(b(F)\).  
  *Use for:* the one-sentence contrast with NBS and the symmetric equal-split note.

### Divide-the-dollar normal form (used in Part 2a)
- **Narahari (2012) lecture notes)** — *The Two Person Bargaining Problem* (sections titled “Nash demand / divide-the-dollar”).  
  *Use for:* the simultaneous-move model: each demands \(x_i\), payoff \((x_1,x_2)\) if \(x_1+x_2\le T\), else \((0,0)\); the **frontier** pure NE \(x_1+x_2=T\) and intuition for multiplicity.

### Interpretation / refinements / dynamics
- **Rubinstein (1982)** *Econometrica* 50(1): **97–109** — alternating-offers; unique **SPNE** depending on discount factors; equal split as players become patient.  
  *Use for:* “realism and multiplicity” paragraph (why sequential institutions select a single outcome).

### Computational tractability / algorithms
- **Duggan (2017)** *Games and Economic Behavior* 102: **111–126** — existence of stationary bargaining equilibria (theoretical backdrop for algorithmic considerations).  
- **Trejo & Clempner (2018)** in *New Perspectives and Applications of Modern Control Theory* (Springer), **pp. 335–369** — computational methods comparing NBS vs. KS in continuous-time controllable Markov games (iterative solvers, regularization).  
  *Use for:* the short “tractability” note linking to algorithmic bargaining solvers.

## Quick mapping to the paper’s sections
- **Equilibrium concept:** cite **Nash 1950 (pp. 155–162)** for definition/axioms; add the plain-language geometry line with **Niederle (slides)**.  
- **Analytical solution (divide-the-dollar):** cite **Narahari (notes)** for the simultaneous-demand formulation and the **frontier NE** characterization; for fairness benchmarks, cite **Nash 1950** and **Kalai–Smorodinsky 1975**.  
- **Interpretation:** multiplicity and refinement via **Rubinstein 1982**; bounded-rationality one-liner via **Niederle (slides)**; tractability pointers via **Duggan 2017** and **Trejo & Clempner 2018**.

## BibTeX
A `references.bib` is included under `refs/`. If compiling in LaTeX:
```tex
\usepackage[backend=biber,style=authoryear]{biblatex}
\addbibresource{refs/references.bib}

