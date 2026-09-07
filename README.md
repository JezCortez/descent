# DESCENT — a tetr.io-style Tetris clone

A fast-paced, single-file Tetris clone with modern guideline mechanics and juicy visual effects. No build step, no dependencies to install — just open the HTML file in a browser.

![status](https://img.shields.io/badge/status-playable-brightgreen) ![platform](https://img.shields.io/badge/platform-browser-blue)

## Play

Open [`tetris.html`](./tetris.html) directly in any modern browser (Chrome, Firefox, Safari, Edge). That's it — no server, no npm install.

```bash
# clone it
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

# then just open the file, e.g. on macOS:
open tetris.html
# or on Linux:
xdg-open tetris.html
# or on Windows:
start tetris.html
```

You can also serve it locally if you prefer (e.g. `python3 -m http.server`) and visit `http://localhost:8000/tetris.html`.

## Features

- **7-bag randomizer** with a 5-piece next queue
- **Hold** with swap-lock (can't hold twice in a row)
- **SRS rotation system** with full wall-kick tables for JLSTZ and I pieces
- **Ghost piece** preview
- **DAS / ARR** movement (auto-repeat on held direction), soft drop, hard drop
- **Lock delay** with move/rotate resets (capped, so pieces can't stall forever)
- **T-spin detection** (mini and full, via the 3-corner rule)
- **Scoring system**: combos, back-to-back bonus, perfect clear bonus, level-based gravity curve
- **Effects**: glowing neon pieces, particle bursts on line clears and hard drops, screen shake, line-clear flash, animated popup text (`TETRIS`, `T-SPIN`, `PERFECT CLEAR`, etc.), combo/back-to-back badges
- **Responsive + touch-friendly**: on-screen control pad and swipe gestures on touchscreens/small screens; full keyboard controls on desktop

## Controls

| Action | Key |
|---|---|
| Move left / right | `←` `→` |
| Soft drop | `↓` |
| Hard drop | `Space` |
| Rotate clockwise | `↑` or `X` |
| Rotate counter-clockwise | `Z` |
| Hold | `C` or `Shift` |
| Pause | `P` or `Esc` |

On touch devices, an on-screen pad appears automatically, and you can also swipe on the board (swipe left/right to move, swipe down to hard drop, tap to rotate).

## Tech stack

Plain HTML, CSS, and vanilla JavaScript — rendered with the Canvas 2D API. No frameworks, no build tools, no external JS dependencies (Google Fonts are loaded via CDN for the UI typography only).

## Project structure

```
.
└── tetris.html   # everything — markup, styles, and game logic in one file
```

## License

MIT — do whatever you'd like with it.
