# Incredulous Knuckles

A [Sonic 3 A.I.R.](https://sonic3air.org/) mod that adds Knuckles as a 3rd AI companion when playing as Sonic & Tails. Knuckles isn't buying Eggman's lies this time — he joins the team from the start.

[![Incredulous Knuckles](https://img.youtube.com/vi/9p2diE-k-NQ/0.jpg)](https://www.youtube.com/watch?v=9p2diE-k-NQ)

## Features

- **3-Character Gameplay** — Sonic, Tails, and Knuckles all on screen at once
- **Character Swapping** — Press Y to cycle control between all three characters
- **3-Person Formations** — Tails can carry a chain of all three characters; Knuckles can glide-carry Sonic
- **Hyper Form for All** — When one character transforms, all three go Hyper with rainbow palettes and Super Flickies
- **Both Paths Unlocked** — Sonic's and Knuckles' paths are accessible in every zone, with player-activated buttons replacing NPC Knuckles cutscenes
- **Blue Spheres Support** — Knuckles appears as a 3rd character in special stages
- **Custom AIZ Intro** — New opening cutscene where Knuckles sees through Eggman's deception

## Installation

1. Download or clone this repository
2. Copy the folder into your Sonic 3 A.I.R. `mods/` directory
3. Enable the mod in the Sonic 3 A.I.R. mod manager
4. Select **Sonic & Tails** as your character — Knuckles joins automatically

## Mod Settings

| Setting | Options | Default |
|---------|---------|---------|
| Knuckles' Sky Sanctuary | Off / On (HPZ teleporter) | Off |
| Hyper Speed | Per-character / Sonic's speed for all | Sonic's speed for all |
| HPZ Mini-Boss | Fight Knuckles / Skip to Robotnik | Skip to Robotnik |
| ERZ Flight Toggle | Off / A button toggles flight | On |
| Hyper Flickies | Off / On | On |

## Compatibility

- Built for Sonic 3 A.I.R. version `24.02.02.0`
- Compatible with the ERZ Flight Revisited mod (use the ERZ Flight Toggle setting)

## Project Structure

```
scripts/
  main.lemon              Master include file
  defines.lemon            Constants, memory layout, utilities
  knuckles_ai.lemon        P3 AI state machine (follow, respawn, glide-in)
  character_swap.lemon     Y-button character cycling
  formation.lemon          3-person carry chain system
  character.lemon          BaseUpdate overrides, control routing, death/respawn
  maingame.lemon           Game loop, slot allocation, initialization
  objects.lemon            P3 collision system + per-object extensions
  super.lemon              Hyper form, rainbow palettes, Super Flickies
  bluespheres.lemon        Blue Spheres special stage P3 support
  ui.lemon                 Swap indicator HUD + character select menu
  zones/                   Per-zone logic (path routing, bosses, cutscenes)
```

## License

[MIT](LICENSE)
