# Sparkle Salon — branch `sparkle-salon`

Playable makeover prototype with eight original character progression states, seven grooming interactions and thirty configured level entries (the task flow currently repeats).

## Web preview
```bash
python3 -m http.server 8000
```
Open `http://localhost:8000/web/`. The mobile-oriented WebP atlas (~43 KB) is cached and used across all seven task steps. Exposed hair targets are used instead of the head towel/band. For an Internet-playable HTTPS link, deploy the `web/` directory to static hosting or GitHub Pages.

## HS Native source
`native/game.js`, `native/game.json`, `native/project.config.json`, and `native/assets/makeover-atlas.webp` are included. Before building the Native game, copy `hs-game.js` and `hs-sdk.min.js` from the provided HS SDK 1.1.3 package into `native/`. The SDK binaries are not republished in this public GitHub repository pending redistributable license verification.

Cloud profile, ads, rewards and shop require real HS/TikTok credentials and device verification.

## Status
Web and Native code are present but the goals of 40+ minutes and IPU 8/5 minutes, plus unique content for all thirty levels, are not validated for release.
