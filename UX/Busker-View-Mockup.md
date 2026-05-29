# Busker View — Mockup

What the end user sees. One screen carries the whole demo.

```
┌─────────────────────────────┐
│  Buskr 🎸        📍 Downtown │
│                              │
│   "I'm free Sat 2–6pm"   ▾   │
│   🎸 Acoustic guitar     ▾   │
│                              │
│  ┌────── MAP ──────────────┐ │
│  │     🟢 Dundas Sq         │ │   🟢 great now
│  │   🟡          🟢 Distillery│   🟡 ok / restricted
│  │      🔴 Kensington       │ │   🔴 illegal now
│  │   🟢 Harbourfront        │ │
│  └──────────────────────────┘ │
│                              │
│  ⭐ Best right now           │
│  ┌──────────────────────────┐│
│  │ Yonge–Dundas Square      ││
│  │ 🟢 Legal til 9pm         ││
│  │ 👣 Peak traffic 5–7pm    ││
│  │ 💰 ~$22–34/hr (acoustic) ││
│  │ 🎤 2 buskers nearby      ││
│  │        [ Plan my day → ] ││
│  └──────────────────────────┘│
└─────────────────────────────┘
```

## The flow
1. **Profile** — instrument(s), genre, setup (amp vs acoustic), gear portability, permit status.
2. **Home = map** of Toronto with spots glowing by a single **Buskr Score** (legality + foot traffic + projected $/hr collapsed into one color).
3. **Tap a spot** → detail card with the legality rule, traffic peak window, projected earnings, nearby buskers.
4. **Plan my day** → the optimizer ([[NVIDIA-Stack|cuOpt]]) returns a *route*: "Distillery 2–4pm → walk 12 min → Dundas Sq 5–7pm. Projected $96."
5. **Ask** → free-text to the [[The-Four-Agents|Legal agent]]: *"Can I use an amp at Yonge-Dundas?"*

## The key idea
Every glowing dot is three agents ([[The-Four-Agents|Legal + Traffic + ROI]]) collapsed into one color. The complexity is real; the surface is dead simple.
