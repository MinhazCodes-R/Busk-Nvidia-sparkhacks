# Assigning Tasks

Team size: **plan for 3** (4th = bonus floater). Everyone is AI-assisted (Claude / coding buddy).

## Guiding principle
With everyone AI-assisted, **raw coding stops being the bottleneck — integration does.** Three people each moving 2× as fast will produce three subsystems that don't fit together unless we force a contract early. So we split by **clean seams**, not equal lines of code.

> Assumes the **Spot + ROI optimizer** hero flow (see [[Open-Decisions]]). If the hero changes, the seams shift.

## The split — by layer, one owner per seam

| Dev | Owns | Deliverable | Why it's a clean seam |
|---|---|---|---|
| **A — Frontend / Product** | Next.js PWA: map with glowing Buskr-Score dots, spot detail card, "Plan my day" route view, the Ask box. *(Stretch: Mission Control desktop view — see [[Form-Factor-Decision]].)* | What judges **see** ([[Busker-View-Mockup]]). | Builds against a **mock JSON file** from minute 1 — never blocked. |
| **B — Agents / Orchestration** | Planner/orchestrator + Legal-RAG agent + ROI logic. Hosts LLMs (NIM). **Owns the API contract** (`/api/recommend`, `/api/ask`). | The "brains" + the glue ([[The-Four-Agents]]). | Sits in the middle → natural **integration owner**. |
| **C — Data / GPU Optimization** | Source + clean Toronto foot-traffic & bylaw data (RAPIDS/cuDF). Build the **cuOpt** spot-ranking + route optimizer. Feed the heatmap viz. | The NVIDIA horsepower ([[NVIDIA-Stack]]). | Exposes one function: `optimize(spots, time, instrument) → ranked spots + route`. |

**4th person, if they show:** don't pre-assign a subsystem. Float to the bottleneck — almost certainly **pairing with Dev C on data** (the usual time sink), or peeling Mission Control off Dev A, or becoming a dedicated **integrator + demo/pitch owner**.

## The 3 non-negotiables
1. **Hour 1, whole team at a whiteboard: lock the JSON contract + data schema.** What does `/api/recommend` take and return? Nothing else starts until this exists. Highest-leverage 45 min of the weekend.
2. **Commit a `mock-recommend.json` immediately.** Dev A and Dev B build against it so they aren't stalled waiting on Dev C's real data + cuOpt (slowest to come online). Swap mock → real at integration.
3. **Each dev pastes the same `CONTRACT.md` into their AI assistant.** Otherwise three assistants invent three slightly-different data shapes and we lose Saturday night to reconciling them.

Plus: feature branches, small PRs, integrate continuously (not Sunday 10am). Assign the **demo driver** Friday; rehearse Sunday AM.

## TODO
- [ ] Draft the actual `/api/recommend` contract (request + response JSON)
- [ ] Confirm hero flow at kickoff ([[Open-Decisions]])
- [ ] Confirm who is Dev A / B / C
