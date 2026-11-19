# ZODRAN: Shadow Protocol
**The city is compromised. Your move.**

An original 3D, story-driven cybersecurity action game built in **Three.js**, designed for the browser. Explore the neon-lit streets of Solara City, collect Z-coins, uncover cybercrime, and grow your operator reputation.

**Playable demo:** https://vincentayorinde.github.io/zodran/

## What's playable (alpha v0.2)

- Fully rendered **3D city** with procedural buildings, neon signs, windows, atmospheric lighting, fog, streetlights and cinematic postprocessing on desktop
- Third-person operator with animated movement, follow camera, walking and sprinting
- **Keyboard controls:** WASD / arrow keys to move, Shift to sprint, E or Space to interact, Escape for menu
- **Mobile touch controls:** Direction pad and interact button
- Three floating signal-beacon mission stations, with sequential unlocks
- **Three story cases and six choices:** Ghost Delivery (phishing), Silent Transfer (invoice fraud), Account Echo (account takeover)
- Evidence inspection, decision consequences, explanations and mission scoring
- **17 collectible Z-coins** with sound cues, XP, unlockable levels and ranks
- Offline **leaderboard preview** with explicitly fictional rivals and the real player's locally saved score
- Reward vault showing earned local credits and their non-cash status
- Persistent callsign, mission best scores, collectibles, XP and credits via `localStorage`
- Optional original synthesized UI sound effects

## Technology

- Three.js **0.187.0** with pinned CDN ES-module import map
- EffectComposer, UnrealBloomPass and OutputPass on desktop; standard renderer on mobile
- Plain HTML, CSS and JavaScript; no React build step, bundler or framework lock-in
- Procedurally generated 3D world; no external textures, paid assets or third-party music
- Browser-local progression (no authentication, backend, database or payout processing)

## Run locally

This is a static website. A local HTTP server is recommended because the Three.js module is imported from a CDN.

```sh
python3 -m http.server 8000
```

Open **http://localhost:8000**. The browser needs a WebGL-capable GPU and internet access for the pinned Three.js dependency.

## GitHub Pages deployment

Repository → **Settings** → **Pages** → Source: **Deploy from a branch** → Branch: `main`, Folder: `/ (root)`.

Any merge or commit to `main` updates the static site. Clear cache/reload after deployment.

## Code structure

```text
index.html              # DOM screen structure / pinned ESM imports
styles.css              # Responsive cinematic game HUD and mission UI
game.js                 # Three.js world, gameplay loop, missions, rewards
.github/workflows/       # Basic validation on push
README.md
```

The current code is a working **vertical slice**, not yet a production-scale persistent multiplayer world. A server-backed leaderboard would require authenticated profiles, server-authoritative mission scoring, request validation, abuse controls and a database. **Do not trust browser-local XP or coins for cash prizes.**

## Safety and money

All cybersecurity scenarios are fictional and use inert `.example` domains. There are no attacks against real systems. Z-credits cannot be withdrawn, purchased, transferred or exchanged for cash. Fictional leaderboard rivals are labelled as such. There is no paid contest.

## Roadmap

1. Test 3D performance on browsers and devices; add quality presets, improve collision and cinematics.
2. Build additional districts, character animations, richer dialogue and collectible cosmetics.
3. Extract the scoring engine into server-validated APIs, then integrate Postgres with optional authentication.
4. Add real leaderboard accounts, fraud controls, content moderation, and only then investigate sponsored competitions.

**Brand note:** ZODRAN is a provisional creative name pending trademark clearance.
