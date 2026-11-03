# Sparkle Salon — Codex Cloud handoff (2026-11-03)

This repository contains the latest GitHub version of Sparkle Salon. **Working branch: `sparkle-salon`**.

## Current delivered code
- Static browser prototype (`index.html`, `web/index.html`) with compact 8-stage makeover artwork, sequential tasks, HTML/JS gesture interactions, before/after and basic 30-level progress.
- WebP atlas in `web/assets/makeover.webp` (about 43 KB); HD asset in `assets/makeover-preview.webp` (about 166 KB).
- Native prototype source in `native/` with Canvas-oriented JavaScript, project configuration, and optimized atlas.

## What is NOT finished
- Native production verification inside TikTok/HS runtime, ad credentials and actual cloud save.
- Robust level variety and balance through all 30 levels; engagement/ad KPIs are goals, not results.
- Pixel-perfect matching of every gameplay hit target and original character. The user identified marks on the pink head wrap as an unacceptable issue for hair detangling.
- Verified iPhone ChatGPT iframe fullscreen: embedded preview can sometimes trigger host chat scroll. Host controls might block Fullscreen API.

## User correction to implement first
Hair detangling: put knots on exposed hair (brown strands above/behind headband, or loose visible side locks) rather than on pink bunny headband. Make comb swipe follow strand direction, show progressive removal, prevent success when scraping the headband. Validate on mobile touch.

## Performance priority
- Inline artwork should load quickly. One compact WebP atlas, preloaded once; avoid embedding duplicate base64 copies.
- Draw/update only when necessary instead of expensive repeated full-canvas rerendering.
- Limit on-screen animation and resize work.
- Pointer capture, `touch-action: none`, and `overscroll-behavior` on the interactive region. Native app fullscreen and ChatGPT iframe fullscreen must be treated separately.

## Typical local run

```bash
git switch sparkle-salon
python3 -m http.server 8000
# http://localhost:8000/web/
```

Web build does not require an npm install. For Native: review vendor SDK integration separately before claiming deployability.

## Product requirements from prior conversation
7 makeover tasks, progressively prettier character images, real interaction; 30 planned levels; later game balancing and ad insertion after initial levels. User expects polished, correct visuals, actual playable artifacts, smooth phone responsiveness, no repeated clarification requests.

## Release acceptance checklist
- First load works on mobile Safari; all 8 frames visibly switch correctly.
- Task 1 knots are on real brown hair, not headband; only correct downward comb strokes count.
- Correct tool enforced for every task.
- Completion only when every target is treated, exactly once reward/state increment.
- All 7 tasks playable sequentially and before/after correct.
- No page scroll during swipes inside game; no clipping or huge layout shifts.
- Code checked and real test evidence attached to PR.
