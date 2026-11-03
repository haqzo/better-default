# Better Default 1.5.0

PokeMMO's default layout, restyled so every classic window matches the new HUD. Version 1.5.0 is the biggest update yet: modern tab rows, rounded progress bars everywhere, a redesigned trainer card, a sparkling login screen, a fully themed contest screen, bigger buttons across the UI and **20 new colour options (56 in total)**.

<!-- drag in: forum/01-login-sparkles.gif -->

## Install / update
1. Close PokeMMO. Delete older Better Default / Midnight `.mod` files from `<PokeMMO>/data/mods/`.
2. Copy `Better-Default-1.5.0.mod` into `<PokeMMO>/data/mods/` (don't unzip it).
3. Start PokeMMO → **Mod Management** → enable **Better Default**.
4. **Settings → Interface → Theme**: pick **Better Default** (or **Better Default (no battle backdrop)**) and restart.
5. **Updating?** Press **Settings → Interface → Theme Settings → Apply Theme Preset** once to load the new colours (your saved colours stay until you do).

> Used **"Better Default + Type Chart"**? That theme entry is gone. The type chart is now built into the main theme: point the mouse at your trainer name on the trainer card. Pick **Better Default** again.

## What's new

### Tabs
- Every tab row (GTL, Mail, Friends, Guild, Pokédex entry, shops, Gift Shop, encounter history…) is one rounded bar. The selected tab is a raised pill, the others use muted text, and the tabs are a little taller.
- **Bag:** every pocket is its own small tab standing on the bag window. The selected pocket is wider and pops up above the others.

<!-- drag in: forum/03-bag.png  +  forum/04-gtl.png  +  forum/10-friends-mail.png  +  github-extra/gift-shop-tabs.png -->

### Progress bars
- Rounded dark track with a flat rounded fill instead of thin striped lines.
- Where: Pokédex totals and base stats, Summary EXP / HP / happiness / contest stats, party and PC bars, request countdowns, matchmaking and the contest love meter.
- A value of 0 shows an empty track. (The HUD event bars keep their look.)

<!-- drag in: forum/07-summary-stats.png -->
<!-- drag in: forum/05-pokedex.png  +  forum/06-pokedex-entry-base-stats.png -->

### Trainer card
- The card has its own PokeMMO wordmark ("MMO" in your Accent), centred over the "Issued" date.
- The Accent line dips under the date, which sits on a soft band.
- Hover your trainer name to see the type chart.

<!-- drag in: forum/02-trainer-card-typechart.gif  +  github-extra/trainer-card.png -->

### Login screen
- The PokeMMO logo sits higher.
- Soft shiny sparkles twinkle around the emblem, subtle and never over the login window. They have their own colour option.

### Pokémon Summary
- The grey top bar is dark blue.
- The value boxes on every page are flat rounded tiles.
- The window, top bar, boxes and the darker Item Held bar each have their own colour.
- "Item Held" and the item slot sit on matching raised tiles, and the item name is bold.

<!-- drag in: forum/08-summary-ivs-item-held.png -->

### Contest
- The whole screen matches battle: theme buttons with centred text, battle bands and panels, and a rounded love meter.

### Berry water tags (Better Water Levels – Fancy by Pancho412)
- Recoloured to the theme: dark tag, drops in the new Berry water colour, dry = red, fully watered = water-coloured tag.

<!-- drag in: forum/12-berry-water.png -->

### More
- **HUD notification badge** (new mail etc.): your Accent colour instead of fixed red.
- **Matchmaking statistics:** the tier tabs use the theme's buttons.
- **Pokédex:** grid outlines and totals bars share one customizable colour each (caught, caught OT, alpha, shiny, costume).
- **Symbol glyphs** (GTL clear / refresh, arrows) follow the Text colour.

<!-- drag in: github-extra/hud-notification-badge.png -->

### Bigger buttons and windows
- **Bigger buttons in:**
  - Login and server select
  - GTL Advanced Search and the clear / refresh buttons (lined up with the dropdowns)
  - Mod Management
  - Client Management
  - Settings Cancel / Save (with a little more room above)
  - Yes / No popups
  - Plant Seeds
  - Matchmaking
  - Pokédex Play Cry / Toggle Shiny
- **Bag:** 3 more rows of items.
- **Pokédex:** about 2.5 more rows of Pokémon.
- **Settings → Interface:** smaller colour pickers (much less scrolling) and shorter option names.

<!-- drag in: github-extra/battle-menu.png -->
<!-- drag in: forum/09-battle-moves.png -->
<!-- drag in: forum/11-matchmaking-pvp-stats.png -->
<!-- drag in: github-extra/plant-seeds.png -->

### Fixes
- Battle HP bar at 0 HP is empty, with no red dot.
- Battle move buttons are no longer squashed the first time you open Fight.
- Progress bars at 0 no longer show a dot.

### Themes
- **Removed:** "Better Default + Type Chart". The type chart is now in the main theme (hover your trainer name).
- **New:** "Better Default (no battle backdrop)", the same theme without the dark band behind the battle buttons and messages.

### Options: 56, was 36
**20 new:**
- Good values / Bad values text
- Tab bar
- Selected tab
- Pokémon Summary window / header / boxes / item bar
- Notification badge
- Trainer card date band
- Battle messages text
- Login sparkles
- Bar tracks
- Pokédex: caught / caught OT / alpha / shiny / costume
- Happiness bar
- Berry water

**Renamed:** "Battle menu backdrop" is now **"Panel backdrops"**, and several names are shorter.

**Presets (all 11):**
- Every preset sets every new option.
- Links, the trainer card logo and date band, the notification badge and the login sparkles follow each preset's Accent.
- Tab bar / Selected tab follow each preset's Text fields / Buttons colours.
- The trainer card logo is now blue (Accent) by default instead of gold.

## Credits
Better Water Levels (Fancy) by **Pancho412** – built in with its layout unchanged, recoloured to match the theme (forums.pokemmo.com/index.php?/topic/187702).

## Under the hood
- **New textures:** `bd-ui-111.png` (bars, card band, wordmark), `bd-water.png` (berry water), `bd-sparkle.png` (login sparkles).
- **New files:**
  - `typechart.xml`: type chart on hover.
  - `no-backdrop.xml` and the `better-default-nobackdrop` theme entry.
- **Removed:** the `better-default-typechart` theme entry.
- **Copies of game themes in `main-widgets.xml`** (they replace the game's versions, so refresh them if a game update changes them):
  - `broker-window`, `battle-frame`, `battle-panel`, `monster-frame`, `settings-colorselector`
  - `mods-panel`, `rom-panel`, `settings-panel`
  - `label-area-monsterdex`, `monsterdex-frame`, `monsterframe-progressbar-contest-2/total`
  - `inventory-tabbedframe`, `inventory-tab-empty`
  - `seed-plant-dialog`, `matchmakingframe`, `matchmaking-stats-frame`, `chat-tab-settings`
  - `contest-button`

Full changelog: see `CHANGELOG.md` in the repo.
