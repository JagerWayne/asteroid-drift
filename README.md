# Drift

A quiet voyage through an asteroid field.

A relaxing, no-fail 3D asteroid shooter that runs entirely in the browser from a
single self-contained HTML file. There is no timer, no game over and no score
you can lose — just you, a hummed engine, two small turrets and a lot of very
slow-moving rock.

**Play it:** https://jagerwayne.github.io/asteroid-drift/

## Features

- **No fail state.** Break rocks, chain the breaks for a multiplier, scoop up
  what the field leaves behind.
- **Two aiming modes.** *Automatic* turrets hunt the best rock ahead and lead
  it; *Manual* lets you place a reticle and the turrets swing to follow it.
- **Free mode (autopilot).** Press `G` (or "let the autopilot fly" on the title
  screen) and the ship flies itself. Any movement key hands control back.
  Autopilot gunnery can be set to *Always*, *When needed* or *Do not shoot*.
- **Power-ups:** rapid fire, spread, ward, magnet, nova.
- **A full settings modal** with staged edits, an Apply button and
  `localStorage` persistence: per-family volume mixers, eleven engine voices,
  HUD visibility, reduced camera motion and more.
- **Procedural everything.** All textures, the celestial generative music
  (pad, bells, arpeggio, chimes and slow swells), the ship, the ringed planet,
  the comets and the dust are generated at runtime. No external assets.

## Controls

| Key | Action |
| --- | --- |
| `W` `A` `S` `D` / pointer | Move |
| `T` | Aim mode (Automatic / Manual) |
| `G` | Free mode (autopilot) |
| `H` | Show / hide HUD |
| `F` | Auto-fire |
| `M` | Mute |
| `P` | Pause |
| `Esc` | Settings (closes / opens) |
| `Enter` | Apply settings (while the modal is open) |

## Running it

Just open `index.html` in a browser. It is a single file with no build step and
no dependencies except Three.js, which is loaded from a CDN.

To serve it locally:

```sh
python -m http.server 8000
# then visit http://localhost:8000
```

## Notes

- Audio starts on the first click (browsers require a gesture before playback).
- Settings are saved to `localStorage`; the best combo score is saved separately.

## Credits

Built by **Grey-Ship** / [JagerWayne](https://github.com/JagerWayne).

Created with AI assistance (an agentic coding session), including the
procedural audio, the ship/turret models and the game logic.
