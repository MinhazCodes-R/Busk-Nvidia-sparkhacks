# NVIDIA Stack

## Why this matters
It's NVIDIA's hackathon. **"GPT wrapper" won't win.** Buskr has a genuine hook into NVIDIA's flagship stack that turns the same idea into a *GPU-accelerated multi-agent optimizer* — same product, 10× the credibility with these judges.

## The mapping
| NVIDIA tech | Buskr use | Role |
|---|---|---|
| **cuOpt** (GPU optimization) | "Find the optimal legal spot + time slot to maximize earnings" is *literally* a constrained optimization / routing problem. | **The hero.** Powers "Plan my day." |
| **RAPIDS / cuDF** | Crunch the Toronto foot-traffic dataset on GPU. | Data layer |
| **NIM microservices** | Host the agent LLMs. | Agent runtime |

## The decision still open
How hard to lean in (all-in cuOpt+RAPIDS+NIM vs. light-touch NIM-only vs. pure GPT wrapper) is an [[Open-Decisions|open call]]. Also need to confirm **what NVIDIA hardware / cloud credits are actually provided at the event** before committing to cuOpt setup.

## Narrative
The [[Form-Factor-Decision|Mission Control view]] is where this becomes *visible* to judges: heatmaps + live optimization animation = proof of GPU horsepower.
