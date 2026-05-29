# Concept

## The pitch
We love music. Toronto has some of the most restrictive and confusing laws around **street busking**: where you can play, when, permit windows, equipment rules. The friction is killing the city's street-music scene.

**Buskr** is a multi-agent app that removes that friction. Tell it what you play and when you're free, and it tells you **where to legally play, when, and what you'll likely earn** — all grounded in real Toronto datasets.

## The core insight
A busker faces the same high-friction decision every single day:

> *"Where can I legally play, when, and will it be worth my time?"*

The answer changes by **location × time × bylaw × foot traffic** — exactly the kind of problem where an agent earns its keep. And the data to answer it already exists publicly:
- Toronto Open Data — pedestrian volume / foot-traffic counts
- TTC Subway Musician permit program (a real, permitted thing)
- City of Toronto busking bylaws

## Why it wins at *this* hackathon
Grounded in **real local data** (judges love this), and it maps cleanly onto NVIDIA's flagship stack — see [[NVIDIA-Stack]]. The architecture is genuinely agentic — see [[The-Four-Agents]].

## Scope discipline
The original vision had four agents. For a 48-hour build, **four agents = four half-broken agents**. The plan is **one killer end-to-end flow** with a multi-agent architecture behind it. See [[Open-Decisions]] for the hero-flow call.

---
*(The billion-dollar a16z/YC round and the $60B SpaceX exit while pre-revenue remain on the roadmap. 😉)*
