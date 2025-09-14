# Behavioral Scientist — README

This folder contains the materials for **Part 3 (Behavioral Scientist)** of the project.

## Deployment (oTree)

**Requirements:** Python 3.10+ and `otree` (v5+).

```bash
python -m venv .venv
. .venv/bin/activate     # (Windows: .venv\Scripts\activate)
pip install otree

### Run Locally

```unzip otree_app.zip -d otree_app
cd otree_app
export OTREE_AUTH_LEVEL=DEMO    # (Windows PowerShell) $env:OTREE_AUTH_LEVEL="DEMO"
otree devserver```

Open the admin URL shown in the terminal. Create a session with the config named, e.g., demand_game.

## Session config (used in our run):

players_per_group = 2 (fixed matching across rounds)

num_rounds = 5

pie_size = 50 (baseline)

Feedback each round: opponent demand, feasibility (bust vs feasible), round and cumulative payoffs

Data captured (per round):
demand_1, demand_2, feasible, payoff_1, payoff_2, cum_payoff_1, cum_payoff_2, timestamp

After the 5th round, we asked 1–2 short post-play questions:
1) When playing the Bargaining game did you find your decisions impacted by the smaller pool of money?
2) When playing the bargaining game, did playing multiple rounds lead you to adapt to the other player’s play style?

## LLM “ChatBot” session (replication)

We played the same 5-round game with ChatGPT vs Claude.
See llm/prompts.txt for the exact instructions and round prompts (identical framing to the human session).
See llm/transcript.md for the complete interaction (stated reasoning, demands, and outcomes each round).
To replicate, reuse the prompts verbatim, keep the opponent fixed across rounds, and reveal each round’s outcome before the next decision.

## Brief ethics note

This classroom activity involved minimal risk. We obtained informed consent, collected no PII, and anonymized decisions. Participation was voluntary with the option to skip questions or withdraw. Data are stored locally for course evaluation only. Any future public use would require appropriate ethics review (e.g., IRB).


