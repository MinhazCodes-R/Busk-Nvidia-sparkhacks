# Form-Factor Decision

## Who's holding the device, and where?
Buskr's user is a busker **standing on a sidewalk with a guitar on their back**, deciding *"where do I go right now?"* — outdoors, on the move, location matters, between sets. Nobody opens a laptop on a street corner.

➡️ **The product is unambiguously phone-facing.** GPS-aware, glanceable, one-handed.

## But "phone-facing" ≠ "native app"
Building a native iOS/Android app is a 48-hour trap: Xcode, provisioning, App Store, and you can't throw it on a projector for judges.

➡️ **Decision: mobile-first responsive web app** (Next.js PWA → Vercel). Looks and feels like a phone app, but it's a URL. Demo it on a real phone, in a phone frame on the projector, or full-screen. Plays to the existing Next.js skillset.

## The power move: dual view
Keep the NVIDIA depth visible without cluttering the consumer experience:

- **📱 Busker view (phone)** — dead simple. A map, glowing spots, "where should I play?" *This is the product.* See [[Busker-View-Mockup]].
- **🖥️ Mission Control (desktop/projector)** — foot-traffic heatmaps, live agent-reasoning trace, the cuOpt route optimization animating. *This is what flexes the [[NVIDIA-Stack]] for judges* — proof there's GPU horsepower under the hood, not just a GPT wrapper.

Consumer simplicity up front, technical depth on the big screen.

## Status
Recommendation made; awaiting final sign-off and a call on whether Mission Control is in-scope for the weekend or post-MVP. See [[Open-Decisions]].
