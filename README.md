# ZODRAN: Shadow Protocol

**The city is compromised. Your move.**

A playable, cinematic cyber-defence game demo with a neon crime-game atmosphere and a clean mission-oriented interface. This is an original fictional educational experience, not affiliated with Mortal Kombat, Grand Theft Auto, or HappyRobot.

## Play

Open `index.html` in a browser. No installation, dependency, build step, account, API key or backend is required.

For local HTTP serving:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Included gameplay

- Atmospheric fictional city with five mapped districts (one playable, four future expansions)
- Operator callsign and browser-local progress
- Three playable missions: Ghost Delivery, Silent Transfer, Account Echo
- Six scored decisions with evidence inspection, explanations and consequences
- Sequential mission unlocking, replayable cases, rank progression, XP and fictional Z-credits
- Responsive layouts and reduced-motion support
- Fictional offline leaderboard and a clearly labelled reward concept preview

## Deploy with GitHub Pages

1. Open **Settings → Pages** for this repository.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose `main` and `/ (root)`, then save.
4. The demo will be at **https://vincentayorinde.github.io/zodran/** when Pages finishes publishing.

No secrets or GitHub Actions workflow are required.

## Safety and reward status

All scenarios use synthetic incidents, inert .example domains and simulated accounts. Nothing in the game submits user data to a server or interacts with a real threat. Z-credits are fictional and cannot be cashed out. No sponsored tournament, real-money prize, payment, wager, or purchase is offered.

## Local storage

The game uses `zodran_demo_v1`. If a player previously opened an earlier ZEKRAN prototype on the same origin, the demo can read the `zekran_demo_v1` save as a migration fallback. Neither key is sent to a server.

## Brand

ZODRAN is a provisional working brand, not a trademark clearance.

## License

No open-source license is granted at this stage. The prototype is intended for product evaluation.
