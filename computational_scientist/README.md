# Computational Scientist — README

This folder contains the materials for **Part 2 (Computational Scientist)**.

## How to run (Colab or local)

### Option A — Google Colab (recommended)
1. Open **`notebook.ipynb`** in Colab.
2. `Runtime → Run all`. The notebook:
   - Builds the **normal-form payoff matrices** `A` and `B` (for the divide-the-dollar game or the 3×3 bimatrix).
   - Runs **NashPy** (`support_enumeration`) and prints equilibria.
   - Provides a small **decoder** to read mixed strategies (e.g., map arrays to supports like `{1:1/3, 3:2/3}`).
3. Take screenshots for:
   - **(i)** The printed matrices (`matrices.png`).
   - **(ii)** The raw solver output and warning (`solver_output.png`).

**Notes:**
- For the divide-the-dollar game, large grids (e.g., `T=50, step=1`) can be slow and produce many equilibria. Use a **coarse grid** (e.g., `step=5`) for quick, clean screenshots.
- The **“even number of equilibria… degenerate”** warning is **expected** for this game class.

### Option B — Local run
``bash
python -m venv .venv
# Windows: .venv\Scripts\activate     macOS/Linux: source .venv/bin/activate
pip install nashpy numpy jupyter
jupyter notebook notebook.ipynb``

Then run the cells as in Colab and capture the same data!

## What to expect

Matrices: The row player’s payoff matrix A and column player’s B. To ensure google colab could run the bargaining game, the pool is limited to 4.

Equilibria:
* Divide-the-dollar: all frontier pure NE (sum equals the pie), plus mixed equilibria; degeneracy warning likely.

## Game Theory Explorer (Part 2b) — screenshots & captions
To ensure Game Theory could calculate the Bargaining game, the pool is limited to two.

GTEBranchingVisual.png
Caption: “GTE extensive form for the 3×3 game. P2’s three decision nodes are joined in one information set, making moves simultaneous. Leaves labeled with 

GTEOutput.png
Caption: “GTE SPNE solution panel. Lists EE1–EE6 with probability vectors over actions (1–3) and expected payoffs. Matches the normal-form equilibria.”

GTEMatrix.png
Caption: "The matrix created by GTE for the bargaining game."

## Tips & troubleshooting

Degeneracy warning (NashPy): This is normal for divide-the-dollar and for matrices with payoff ties. Include it in the screenshot.

Slow solver on big grids: Increase step (e.g., 5) or reduce T (e.g., 6 or 10).
