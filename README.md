# Coloricious

A browser-based color-matching puzzle game. Six connected panels, each a 3×3 grid of colored tiles, are laid out flat in a cross pattern. Slide rows and columns to mix and unmix the colors — the goal is to make every panel a single, solid color.

## Play Now

Open [`index.html`](https://milohoffman002.github.io/coloricious/) in your browser to start playing!

## How It Works

The game presents six interconnected panels arranged in a cross shape:

```
       [ top ]
[left] [front] [right] [back]
       [bottom]
```

Each panel starts as one solid color. After shuffling, the tiles are scrambled across all six panels. Players drag rows horizontally or columns vertically to slide tiles. Because the panels are connected, tiles flow seamlessly from one panel into its neighbor — every move affects multiple panels at once.

The underlying mechanics are mathematically equivalent to a real-world 3D rotating puzzle, but flattened into a 2D interface that's playable entirely with drag gestures.

## Features

- **Drag-to-slide interaction** — grab any tile and drag horizontally or vertically to rotate that row or column across connected panels
- **Full puzzle math** — all 18 possible slice rotations (6 faces × clockwise/counter-clockwise, plus 3 middle slices) are implemented
- **Touch and mouse support** — works on desktop and mobile
- **Starfield background** — toggle a gentle animated starfield with color wash atmosphere using the ✦ button
- **Sound effects** — synthesized slide sounds on every move, chimes on panel completion, and a melody on full solve (Web Audio API, no external files)
- **Panel completion animation** — when any panel becomes a single color, its tiles play a celebratory bounce animation
- **Full solve celebration** — confetti, ascending melody, and a pulse animation when all six panels are solved
- **Instructions modal** — the ? button opens a plain-language guide to the game
- **Move counter** — tracks how many moves you've made
- **Shuffle & Reset** — scramble the puzzle or restore it to its solved state

## Getting Started

No build step, no dependencies, no server required. Just open the file in a browser:

1. Download `coloricious.html`
2. Open it in any modern browser (Chrome, Firefox, Safari, Edge)
3. Click **Shuffle** and start solving

## Tech Stack

- **Single HTML file** — all markup, styles, and logic in one self-contained file
- **Vanilla JavaScript** — no frameworks or libraries
- **CSS animations** — all visual effects handled with CSS keyframes and transitions
- **Web Audio API** — procedurally generated sound effects with no external audio files
- **Canvas API** — starfield background rendered on a `<canvas>` element

## Controls

| Action | How |
|---|---|
| Slide a row | Drag any tile left or right |
| Slide a column | Drag any tile up or down |
| Shuffle the puzzle | Click the **Shuffle** button |
| Reset to solved state | Click the **Reset** button |
| Toggle starfield background | Click the **✦** button (top-right) |
| Open instructions | Click the **?** button (top-right) |

## Project Structure

```
coloricious.html    — The entire game (single file)
README.md           — This file
```

## Browser Support

Any modern browser with ES6 and Web Audio API support:

- Chrome 60+
- Firefox 55+
- Safari 14+
- Edge 79+

## License

(MIT)[../LICENSE] .. Free to use, modify, and distribute.
