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
  screen) and the ship flies itself. Any movement key hands control back. When
  Free mode starts, a small chooser pops up so you can set the aiming style and
  the autopilot gunnery (Automatic/Manual and Always/When needed/Do not shoot),
  then press **OK**. Tick "Ask me when Free mode starts" off to skip it.
  Entering Free mode also drops into a calm preset — effects off, just the Pad
  music layer at 40%, HUD hidden and control hints off. Your own mix is parked
  and restored the moment you take the stick back.
- **Power-ups:** rapid fire, spread, ward, magnet, nova.
- **A glass-cockpit interface.** The title screen, HUD, settings and touch
  controls share one calm, frosted-glass design — thin uppercase labels,
  generous spacing and a single cyan accent that matches the field.
- **Full screen button** in the bottom-right, next to Settings. It toggles
  fullscreen (with the vendor fallbacks) and re-fits the view the moment the
  size changes.
- **A full settings modal**, organised into categories (Audio, Music, Engine,
  Gameplay, Display, Controls) with staged edits, an Apply button and
  `localStorage` persistence.
- **A real music mixer.** The generative score is split into layers — pad,
  bells, bass, arps, chimes and swells — and every layer has its own on/off
  switch and volume slider under Music. Eleven engine voices, a per-family
  effects mix, HUD visibility, a toggle for the on-screen control hints,
  reduced camera motion and more.
- **Mobile and touch ready.** A responsive HUD and a full touch scheme: drag
  anywhere to steer, a *Fire* button to shoot and a *Free* button to hand over
  to the autopilot.
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

On a touch screen: drag anywhere to steer, and use the on-screen **Fire** and
**Free** buttons.

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
