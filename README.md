# Royal Flush Casino

Static vanilla HTML casino prototype. Open `index.html` directly or serve the
folder from GitHub Pages.

## Canonical entrypoint

- `index.html` is the deployable app.
- The other HTML files are historical variants and are not required to run the
  current version.

## Provided assets

- `assets/symbols/classic.png`, `luxury.png`, `neon.png`: 1280x1280 PNG symbol
  sheets. The app treats each file as a 3x3 grid and uses CSS background
  positioning to render individual reel symbols.
- `assets/mascots/mascot_dealer_spritesheet.png`,
  `mascot_showgirl_spritesheet.png`, `mascot_lion_spritesheet.png`: mascot
  sheets used by the in-game mascot picker. Each mascot sheet is treated as a
  3x3 grid for 9 equal animation frames.
- `assets/audio/dealer_win.mp3`, `showgirl_win.mp3`, `lion_win.mp3`: mascot win
  audio. Browsers may block playback until the user interacts with the page.
- `assets/bonus_wheel.png`: bonus wheel image.
- `assets/bingo_card.png`: bingo card background.
- `assets/lobby/lobby_walk_16.png`: walking lobby character animation sheet.
  The app treats it as 12 equal frames arranged in a 6x2 grid and triggers it
  during loading/spin moments.

## Features

- Classic 3-reel slot.
- High-Roller 3-reel slot.
- Neon 5-reel slot with 3 visible rows, paylines, bonus wheel, and bingo bonus.
- Credits, bet controls, max bet, daily bonus, mascot picker, triggered sprite
  reactions, win effects, sound toggle, and local persistence through
  `localStorage`.

## Local test

From this folder:

```sh
python3 -m http.server 4173
```

Then open `http://localhost:4173/`.

Check that the browser console has no missing asset errors, then smoke test
machine switching, spins, bet controls, the paytable, mascot switching, the
daily bonus, and the Neon bonus surfaces.

## Effect test mode

Open `http://localhost:4173/?test=1` to show direct effect trigger buttons for
win bursts, reel stop pulses, bingo, wheel, character, and lobby walking effects.
