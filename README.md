# Better Default 🌟

**A complete UI restyle for PokeMMO – bringing the entire interface in line with the new HUD.**

When the new HUD dropped on October 30th, I immediately loved its clean and modern look. However, I noticed that the rest of the interface still felt like the original game.

Opening the Bag, Pokédex, Pokémon Summary or entering a battle felt like switching between two different interfaces.

So I decided to change that.

**Better Default brings the entire PokeMMO interface together**, restyling the original UI to match the new HUD while keeping the familiar default layout intact.

No rearranging windows, no relearning menus and no unnecessary changes to how you play. Just a more consistent visual experience.

## ✨ What's Changed?

The goal was to make the entire interface feel like one cohesive design.

- **Windows, menus & popups:** Rounded panels, thin borders and clean title dividers.
- **Buttons, tabs & lists:** Consistent flat styling; hover and selected states use your Accent colour.
- **Close buttons:** Clear red X buttons across all windows.
- **Top HUD:** Location, time and money displayed on a glass-style panel for better readability.
- **Battle UI:** Dark glass nameplates with softened corners, pill-shaped HP/EXP bars, an ability banner in your Accent colour, clean stat badges (+1 Atk / -1 Def), flat Back / Confirm / Register Battle buttons and colour-coded effectiveness labels.
- **Battle Bag:** Flat item list with the selected item in your Accent colour, centred page arrows that light up on hover and an outline-only look when you can't page further.
- **PC & Egg Incubators:** Flat rounded slots; selection and cursor in your Accent colour, search matches in soft green.
- **Pokémon Summary:** Cleaner tab icons with an illuminated selected state, flat dot-grid move buttons.
- **Pokédex:** The Pokémon sprite sits in a clean rounded card.
- **Trainer Card:** Redesigned to fit the overall theme.
- **Login Screen:** Solid background with a slowly rotating emblem behind the login window and a clean PokeMMO logo.
- **Tooltips, chat bubbles & NPC dialogue:** Restyled with matching dark panels.
- **Berry Farming:** Improved water drops, courtesy of Pancho412 (see credits).

---

## 🎨 Fully Customizable

**Settings → Interface → Theme Settings**

Better Default includes extensive customization options, allowing you to create your own look without modifying theme files. New elements follow these options too – for example, the ability banner, PC selection, list highlights and battle buttons all follow your **Accent** and **Battle plates & buttons** colours.

**36 colour options**, covering:

- Accent colours
- Window backgrounds
- Buttons and borders
- Text colours
- HUD panels
- Encounter counter
- Battle interface
- HP bars and more

**11 built-in presets:**

1. Better Default
2. PokeMMO Gold
3. Amethyst
4. Emerald
5. Sakura
6. Ember
7. Arctic
8. Crimson
9. Graphite
10. OLED Black
11. Colourblind-friendly HP bars

---

## 📊 Optional: Better Default + Type Chart

There's also an optional version of the theme!

Selecting **Better Default + Type Chart** from the theme list adds a type chart underneath your Trainer Card.

- Covers all 17 PokeMMO types.
- Checked against the PokeMMO Wiki.
- Integrated into the theme's visual design.

---

## 📋 Changelog

# Better Default 1.5.0 — changelog (everything since 1.1.0)

1.5.0 follows 1.1.0 directly (the 1.1.1 test builds were never released), so this lists every change since 1.1.0.
Compared file by file against the released `Better-Default-1.1.0.mod`.

## New look

### Tabs (every tab row)
- Every horizontal tab row is one rounded dark bar. The selected tab is a raised rounded pill inside it, 3px from the bar on every side.
- Unselected tabs use the Muted text colour. Selected and hovered tabs use the Text colour, and hover shows a faint pill.
- Tabs are a little taller: 28px, was 24px.
- Where: GTL, Mail, Friends, Guild, Pokédex entry, shops, Gift Shop, encounter history, statistics windows and every other tabbed window.
- Left-hand menus (Settings, Matchmaking, PvP Statistics, chat tab settings) keep their own look.

### Bag pockets
- Each pocket is its own small tab standing on the Bag window, with a small gap between pockets.
- The selected pocket is wider and pops up 5px above the others. Hover makes a pocket lighter.
- Pocket icons sit centred. The Bag window, title and search box stay exactly where the game puts them.

### Progress bars
- Every bar is a rounded dark track with a faint edge and a flat rounded fill, instead of thin striped lines.
- Where: Pokédex totals (Seen, Owned…), Pokédex base stats, Summary EXP / HP / happiness / contest stats, party and PC bars, request countdowns, matchmaking and the contest love meter.
- A value of 0 shows an empty track, with no leftover dot.
- The HUD event bars (wisps, raids) keep their look.

### Trainer card
- The card has its own PokeMMO wordmark: "Poke" in the Titles colour and "MMO" in the Trainer card logo colour, which is your Accent by default.
- The wordmark is centred over the "Issued" date.
- The Accent line dips in a smooth curve under the date, and the date sits on a soft band (new option: Trainer card date band).

### Login screen
- The PokeMMO logo sits 36px higher.
- Soft, shiny 4-point sparkles twinkle around the emblem. Each one has its own timing, they fade in and out gently, and they stay clear of the login window, logo, announcements and side buttons.
- New option: Login sparkles. By default it is your Accent mixed with white.

### Pokémon Summary
- The grey top bar is dark blue and has its own colour (Pokemon Summary header).
- The value boxes on every page (overview, stats, IVs, Information, Particles) are flat rounded tiles with a faint edge, instead of bevelled boxes (Pokemon Summary boxes).
- The whole window body follows a new option, Pokemon Summary window.
- The Item Held bar is darker (Pokemon Summary item bar). "Item Held" and the item slot sit on matching raised tiles, and the item name is bold.

### Contest screen
- It matches battle: theme buttons with properly centred text, battle-style top and bottom bands, the opponent box in the battle panel style, and the rounded love meter (Muted text colour, with gains in Accent).

### Berry water tags (Better Water Levels – Fancy by Pancho412)
- Same Fancy shapes and positions, recoloured to the theme: dark tag with a faint edge, full drops in the new Berry water colour, empty drops dark, dry = red (HP bar – critical), and fully watered = a water-coloured tag with white drops.

### Smaller touches
- HUD notification badge (new mail etc.): now the Accent colour (option: Notification badge) instead of fixed red.
- Matchmaking statistics: the tier tabs use the theme's buttons.
- Pokédex: the grid outlines (caught, caught OT, alpha, shiny, costume) and the matching totals bars share one colour each, all customizable.
- Symbol glyphs (GTL clear / refresh, arrows) follow the Text colour.

## Bigger buttons and windows
- **Login and server select:** Forget Saved Password and LOGIN.
- **GTL:** Advanced Search and the clear / refresh buttons, with bigger symbols, lined up with the 28px dropdowns.
- **Mod Management:** the row buttons (Delete Mod, Web Link, arrows) and the bottom bar (Get Mods, Import Mod, Open Mods Folder, Save), 3px apart.
- **Client Management:** Open Roms Folder, Close, Select File and Info.
- **Settings:** Cancel / Save, with 4px more room above them.
- **Yes / No popups.**
- **Plant Seeds:** Plant Seeds / Cancel.
- **Matchmaking:** spectate pages, refresh and the rest.
- **Pokédex entry:** Play Cry / Toggle Shiny.
- **Bag:** 3 more rows of items.
- **Pokédex:** about 2.5 more rows of Pokémon.
- **Settings > Interface:** smaller colour pickers (the game's were 210×128 per option), so there's much less scrolling, and shorter option names so all boxes line up.

## Fixes
- **Battle HP bar at 0 HP:** it's empty now, with no red dot.
- **Battle move buttons:** they're no longer squashed the first time you open Fight.
- **Progress bars at 0** (e.g. contest stats): they no longer show a dot.

## Themes
- **"Better Default + Type Chart" removed:** the type chart is part of the main theme now. Point the mouse at your trainer name on the trainer card and the chart appears below the card. It covers all 17 types with Gen 2–5 rules. If you used the Type Chart theme, pick "Better Default" again.
- **New "Better Default (no battle backdrop)":** the same theme without the dark band behind the battle buttons and messages.

## Options: 56, was 36
**20 new:**
- Good values (green text): 31 IVs, max EVs, GTL
- Bad values (red text)
- Tab bar
- Selected tab
- Pokemon Summary window
- Pokemon Summary header
- Pokemon Summary boxes
- Pokemon Summary item bar
- Notification badge
- Trainer card date band
- Battle messages text
- Login sparkles
- Bar tracks (empty part of every bar)
- Pokedex: caught
- Pokedex: caught OT
- Pokedex: alpha
- Pokedex: shiny
- Pokedex: costume
- Happiness bar
- Berry water

**Renamed:**
- "Battle menu backdrop" → "Panel backdrops" (it still colours battle dialogs, PC, mail and chat panels).
- Shorter names: Selection highlight, Muted text, Tooltip & bubble text, Top bar backdrop, Super effective, Not very effective, No effect.

**Default changes:**
- Trainer card logo is blue (Accent) instead of gold.
- Links are the Accent + 25% white.

**Presets (all 11, in both themes):**
- Every preset sets every new option.
- These follow each preset's Accent: Links, trainer card logo, date band, notification badge, login sparkles.
- Tab bar and Selected tab follow each preset's Text fields and Buttons colours.
- Every preset was checked for readability: all text is at least 6.5:1 contrast on its background.

**Updating from 1.1.0 or older:** Settings > Interface > Theme Settings > **Apply Theme Preset** loads the new colours. Your saved colours stay until you press it.

### Version 1.1.0 – The Modern Update ✨

**Battle**
- Softened corners on all battle nameplates (single, double, horde and raid).
- HP and EXP bars are now rounded pills with a thin border – still readable at 1 HP.
- The ability banner (e.g. "Breloom's Poison Heal") follows your Accent colour.
- Stat badges (+1 Atk / -1 Def) keep an even border at any width; boosts are green, drops are red.
- Back, Confirm and Register Battle buttons are flat like FIGHT / BAG, with an Accent outline on hover.
- Battle bag: flat item list, selected item in your Accent colour, centred page arrows that light up on hover and an outline-only look when you can't page further.

**Windows**
- PC boxes & Egg Incubators: flat rounded slots instead of glows; selection and cursor in your Accent colour, search matches in soft green.
- Pokémon Summary: flat dot-grid move buttons with a rounded end; the highlighted move follows your Accent colour.
- Pokédex: rounded card around the Pokémon sprite.
- Shiny encounter window: dark header (the title was hard to read).
- Small list buttons (PC, Settings, Advanced Search…) share the new flat style.

**Other**
- Login screen: removed the line under the PokeMMO logo.
- The mod info now links to the forum thread.

### Version 1.0.1 – Halloween Update 🎃

- Updated the theme for the Halloween Event (theme revision 10).

### Version 1.0 – Initial Release

- Complete UI restyle to match the new HUD.
- Added 36 customizable colour options.
- Added 11 built-in colour presets.
- Redesigned Battle UI, Trainer Card and Pokémon Summary.
- Updated windows, menus, buttons and popups.
- Added optional Better Default + Type Chart version.

## 📥 Download & Installation

**Latest Version: 1.5.0**

[Download the latest release](https://github.com/haqzo/better-default/releases/latest)

### Installation

1. Download `Better-Default-1.5.mod`.
2. Place it inside `PokeMMO/data/mods/`. **Do not unzip it.** Remove any older Better Default `.mod` first.
3. Start PokeMMO and enable Better Default under Mod Management.
4. Navigate to **Settings → Interface → Theme**.
5. Select either Better Default or Better Default + Type Chart.
6. Restart the game.

### Poke-Manager Support

A big thanks to TheMatthew562 for making the theme available through Poke-Manager!

[Check out Ryukotsuki's Poke-Manager](https://forums.pokemmo.com/index.php?/topic/174159-ryukotsukis-poke-manager/)

---

## 💫 Credits & Thanks

### Pancho412 – Better Water Levels (Fancy)

The improved berry water drops included in Better Default come from Pancho412's Better Water Levels (Fancy) mod.

It's a great improvement for berry farming, and I wanted to include it in this theme.

Please check out the original work and show some support!

[Original Better Water Levels thread](https://forums.pokemmo.com/index.php?/topic/187702-pc-mobile-better-water-levels/)

**Theme foundation:** PokeMMO Default Theme.

---

## 💬 Feedback & Suggestions

If you encounter bugs, have suggestions or think something could be improved, feel free to leave a comment on the forum or open an issue here.

Screenshots of your custom colour combinations are also very welcome. I'd love to see what everyone comes up with!

**Enjoy Better Default! ✨**

---

**PokeMMO Forum Thread:** [Visit the official release thread](https://forums.pokemmo.com/index.php?/topic/201443-pc-better-default-the-whole-ui-restyled-to-match-the-new-hud-%F0%9F%8E%83-updated-for-halloween-%F0%9F%8E%83/)

— **Haqzo**
