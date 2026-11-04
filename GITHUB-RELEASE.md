# Better Default 1.5.5

PokeMMO's default layout, restyled so every classic window matches the new HUD. 1.5.5 is a polish update on top of 1.5.0: a cleaner Bag, white battle labels, better alignment in Mail, PC, Egg Incubators and the Pokédex, two new versions with the game's own login screen, and **3 new colour options (59 in total)**.

## Install / update
1. Close PokeMMO. Delete older Better Default / Midnight `.mod` files from `<PokeMMO>/data/mods/`.
2. Copy `Better-Default-1.5.5.mod` into `<PokeMMO>/data/mods/` (don't unzip it).
3. Start PokeMMO → **Mod Management** → enable **Better Default**.
4. **Settings → Interface → Theme**: pick one and restart:
   - **Better Default**: the theme
   - **Better Default (no backdrop)**: without the dark band behind the battle buttons and messages
   - **Better Default (game login)** / **Better Default (no backdrop, game login)**: the same, with the game's own animated login screen
5. **Updating?** Press **Settings → Interface → Theme Settings → Apply Theme Preset** once to load the new colours (your saved colours stay until you do).

> "Better Default (no battle backdrop)" is now called **"Better Default (no backdrop)"**. If your theme switched back after updating, just pick it again.

## What's new in 1.5.5

### Battle
- The effectiveness labels (Status, Effective, Not very effective, Super effective, No effect) have **white text**, on the same coloured pills.
- **Super effective** and **Not very effective** are a touch lighter and match each other: the same soft tint with a glowing rim.
- "Effective" no longer looks greyed out.
- New option: **Effectiveness text**.

### Bag
- The pockets sit in **one bar on top of the window**, like every other tab row. The selected pocket is a raised pill, and the game world no longer shows between the pockets.
- The bar has the same colour as the search box, and the icons sit centred.
- A **header band** behind "Bag - ITEMS" and the search box (new option: **Bag header**).
- The window body is a touch darker (new option: **Bag window**).
- Item slots use the **same tile as the hotbar**.

### Alignment
- **Pokédex › Wild Locations:** the table lines up with the season tabs on the right.
- **Mail:** square checkboxes with room on the left; names and subjects no longer touch the row edge.
- **Egg Incubators:** a gap between Remove All and Fill All.
- **PC:** gaps between the box buttons, and evenly spaced Pokémon slots (same gap across and down).

### Game login versions
- **"Better Default (game login)"** and **"Better Default (no backdrop, game login)"** show the game's own animated login scene. Windows, buttons and the logo stay themed.
- Why: when you enter the game, PokeMMO draws its own login scene for a single frame with no theme at all, so with the Better Default login background it flashes for a moment. No theme can cover that frame; these versions avoid it.
- They don't have the Login screen background / Login sparkles options.

### Options: 59, was 56
- **3 new:** Bag window, Bag header, Effectiveness text.
- All 11 presets set them in every version: Bag window = the preset's Window a touch darker, Bag header = the preset's Summary header, Effectiveness text = the preset's Text.

## Credits
Better Water Levels (Fancy) by **Pancho412** – built in with its layout unchanged, recoloured to match the theme (forums.pokemmo.com/index.php?/topic/187702).

## Under the hood
- **New texture:** `res/bd-bagbar.png` (pocket bar and header band).
- **New files:** `default-login.xml`; theme folders `better-default-defaultlogin/` and `better-default-nobackdrop-defaultlogin/`.
- **Changed textures:** `effectivity_buttons_en/es/fr/zh.png` (white label text), `pc_slots.png` (slots 3px wider).
- **New copies of game themes in `main-widgets.xml`** (they replace the game's versions, so refresh them if a game update changes them): `wildlocations`, `mail-inner`, `read-mail`, `write-mail`, `incubator-frame`, `inventory-button`. `pc-frame` is extended (only `pc-box-button` changes).

Full changelog, including everything in 1.5.0: see [CHANGELOG.md](CHANGELOG.md).
