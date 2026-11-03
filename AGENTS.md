# Sparkle Salon — Codex Cloud working instructions

You are continuing an existing mobile-first makeover game, not starting a new game. Communicate with the user in Vietnamese, focus on executable results, and do not claim anything was tested unless it was tested.

## Project paths
- `index.html`: top-level static web preview.
- `web/index.html`: web preview.
- `web/assets/makeover.webp`: lightweight 8-frame sprite atlas (4 columns x 2 rows).
- `assets/makeover-preview.webp`: higher-resolution atlas for local/reference use.
- `native/game.js`, `native/game.json`, `native/project.config.json`, `native/assets/makeover-atlas.webp`: existing TikTok Native Canvas-oriented prototype. Native code should be checked against the user's HS SDK 1.1.3 before any publishing claim.

## User's non-negotiables
1. A polished, functional, portrait 9:16 mobile makeover game, with touch interactions and a playable preview.
2. Same bunny-headband girl throughout the makeover: 8 states, beginning messy and ending polished. Each of seven tasks completes part of the transformation.
3. Hair detangling marks MUST be on actual visible hair knots/strands, NEVER on the pink bunny headband or towel. User drags the comb *through the marked hair knot in the indicated direction*; interactions should be spatially accurate.
4. Seven sequential interactive tasks: detangle hair; clean face; spot-care; shape eyebrows; under-eye care; style hair; makeup/final reveal. Require proper tools, directions, hit targets, and smooth feedback.
5. Smooth on iPhone in ChatGPT: small WebP sprites, progressive/lazy loading, predecode image, event-handling with pointer capture + touch-action:none and overscroll containment, layout avoiding host scrolling. Do not assume programmatic fullscreen is available inside ChatGPT's iframe/app.
6. 30-level progression with genuinely escalating challenges eventually; easy 1-2, medium 4-5, harder 9, very hard 10, recovery 11 etc. Current prototype reuses the same level flow; label it a prototype until more varied content is implemented.
7. User expects inline playable artifact within ChatGPT for demonstrations, not sandbox file links that open blank preview on iPhone. Outside ChatGPT, host the web game on HTTPS and verify on iOS Safari.
8. Keep production code, assets, preview files, build instructions, and realistic test reports together. Do not invent HS SDK validation, launch credentials, ads availability, production readiness, or game metrics.

## Previously established integration targets (NOT all implemented/verified)
- TikTok Native Canvas + HS SDK version 1.1.3.
- Cloud save. No login button. Conflict UI text: 'summary level' approach.
- Hide shop until products exist.
- No interstitials in first 3 levels; at least 90 sec between interstitial ads; 30 sec cooldown for rewarded ads; rewards paid once.
- Engagement target >=40 min and IPU 8/5min, both unverified and not guaranteed.

## First steps
1. Check out branch `sparkle-salon` (do not accidentally work on `main`), list files and inspect working version.
2. Run the web preview via `python3 -m http.server 8000` from repo root and view `/web/`. Test all 7 tasks and before/after.
3. Fix precise hair-knot geometry (face vs headband) and pointer interactions first. Choose coordinates based on the actual atlas image pixels.
4. Improve rendering and loading on iPhone, test gesture locking and screen proportions, and produce screenshots/screenscreen recording evidence.
5. Integrate and validate TikTok Native only with actual HS SDK files and real runtime. Report missing inputs honestly.
6. Commit clean changes to a feature branch or this branch as appropriate; keep handoff notes up to date.

Reference: `docs/CODEX_CLOUD_HANDOFF.md`.
