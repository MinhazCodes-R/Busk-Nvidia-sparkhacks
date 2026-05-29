# The Four Agents

Buskr's vision is a set of cooperating agents, each solving one busker problem, under one orchestrator.

| Agent | Job | Hackathon priority |
|---|---|---|
| ⚖️ **Legal / Permit** | "Can I play *here*, at *this* time? What's the rule? What permit do I need?" RAG over Toronto busking bylaws + TTC program. | **Core** — folds in as a legality gate |
| 📍 **Spot Finder** | Find spots with ideal foot traffic for a given time. GPU-accelerated optimization. | **Hero candidate** ([[NVIDIA-Stack]]) |
| 💰 **ROI Estimator** | Project $/hr earnings for a spot/time/instrument from historical patterns. | **Core** — the payoff number |
| 🎤 **Jam Matchmaker** | Match buskers by genre/skill/location to play together. | **Defer** — network-effects feature, hard to demo with zero users |

## Orchestration story
A **planner agent** routes a single user request through the Legal, Spot, and ROI agents and collapses their outputs into one answer (e.g. each glowing dot on the map = all three agents resolved into one color). This keeps the "agentic system" narrative intact even though the *demo* shows one clean flow.

## The trap to avoid
Building all four shallowly → nothing works on stage. Pick the hero in [[Open-Decisions]] and make it bulletproof end-to-end.
