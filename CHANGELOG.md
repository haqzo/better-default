# Better Default changelog

## 1.6.0 — compatibility & polish

### Game update compatibility
- Rebuilt on the updated game default theme for the current client (theme revision 11), including the updated fonts, HUD fonts, HUD atlas, widgets and mail reward slot.

### Pokémon Summary
- The Summary window now has rounded corners and the same faint edge used by the rest of the theme.
- The Pokémon display sits in its own rounded box with a soft rim, together with the Item Held bar.

### PC Deposit Box
- The window contents sit 10px lower, so they no longer run into the title bar.
- Added rounded corners and a faint border.

### Gift Shop
- Buy buttons on sprite cards (Specials, Vanity Items and other categories) now match the size of the other cards.

### Login
- Added a 4px gap between the side-menu buttons (Repair Client … Exit), removing the doubled edges.

### Settings
- Settings > Other now uses narrower value columns, so every column fits inside the window.

### Battle bag
- Added a 4px gap between item rows.

### GTL
- Page buttons (<< 1 2 3 … >>) are slightly larger.

### Theme versions
- Four versions remain available: Better Default, Better Default (no backdrop), Better Default (game login), and Better Default (no backdrop, game login).
- The two game-login versions use the game's own animated login scene and do not include the Login screen background / Login sparkles options (57 colour options rather than 59).

### Customization
- No new colour options in 1.6.0.
- The theme retains 59 colour options in the two standard login versions and 57 in the two game-login versions, with 11 presets.

# Better Default changelog

## 1.5.5 — polish (everything since 1.5.0)

### Battle
- The effectiveness labels (Status, Effective, Not very effective, Super effective, No effect) have **white text**. The coloured pills stay.
- New option **Effectiveness text** (by default each preset's Text colour).
- "Effective" no longer looks greyed out (its text was partly see-through in the game's image).
- **Super effective** and **Not very effective** are a touch lighter and match each other: the same soft tint with a glowing rim.

### Bag
- The pockets sit in **one bar on top of the window**, like every other tab row. The selected pocket is a raised pill, and the game world no longer shows between the pockets.
- The bar has the same colour as the search box. Pocket icons sit centred in it.
- A **header band** sits behind "Bag - ITEMS" and the search box (new option: **Bag header**, by default each preset's Summary header colour).
- The window body is a touch darker (new option: **Bag window**).
- Item slots use the **same tile as the hotbar** (HUD tiles & slots colour).

### Alignment
- **Pokédex › Wild Locations:** the table's right edge lines up with the season tabs.
- **Mail:** square checkboxes with room on the left; names and subjects sit 6px from the row edge, like the date on the right (Inbox and Sent Mail).
- **Egg Incubators:** a gap between Remove All and Fill All.
- **PC:** gaps between the box buttons; Pokémon slots are evenly spaced (6px across and down, was 9px across and 6px down).

### Themes (now 4 versions)
- **New: "Better Default (game login)"** and **"Better Default (no backdrop, game login)"**. They show the game's own animated login scene; windows, buttons and the logo stay themed.
  - Why: when you enter the game, PokeMMO draws its own login scene for one single frame with no theme at all, so with the Better Default login background it flashes for a moment. No theme can cover that frame; these versions avoid it.
  - They don't have the Login screen background / Login sparkles options (57 options).
- **Shorter names** so they fit the Settings list: "Better Default (no battle backdrop)" is now **"Better Default (no backdrop)"**. If your theme switched back after updating, pick it again.

### Options: 59, was 56
- **3 new:** Bag window, Bag header, Effectiveness text.
- Every preset (all 11, in all 4 versions) sets them: Bag window = the preset's Window a touch darker, Bag header = the preset's Summary header, Effectiveness text = the preset's Text.
- **Updating:** Settings › Interface › Theme Settings › **Apply Theme Preset** loads the new colours.

### Under the hood (for GitHub)
- **New texture:** `res/bd-bagbar.png` (pocket bar and header band shapes).
- **New files:** `default-login.xml`, theme folders `better-default-defaultlogin/` and `better-default-nobackdrop-defaultlogin/`.
- **Changed textures:** `effectivity_buttons_en/es/fr/zh.png` (white label text), `pc_slots.png` (slots 3px wider).
- **New copies of game themes in `main-widgets.xml`:** `wildlocations` (monster-dex.xml), `mail-inner` / `read-mail` / `write-mail` (social.xml), `incubator-frame` (incubator.xml), `inventory-button` (inventory.xml). `pc-frame` is extended (only `pc-box-button` changes). `inventory-tab-empty` border is now `6,20,4,20`.
- Removed: the 1.5.x test theme entry (never released).

## 1.5.0 — everything since 1.1.0

1.5.0 follows 1.1.0 directly (the 1.1.1 test builds were never released), so this lists every change since 1.1.0.
Compared file by file against the released `Better-Default-1.1.0.mod`.

### New look

#### Tabs (every tab row)
- Every horizontal tab row is one rounded dark bar. The selected tab is a raised rounded pill inside it, 3px from the bar on every side.
- Unselected tabs use the Muted text colour. Selected and hovered tabs use the Text colour, and hover shows a faint pill.
- Tabs are a little taller: 28px, was 24px.
- Where: GTL, Mail, Friends, Guild, Pokédex entry, shops, Gift Shop, encounter history, statistics windows and every other tabbed window.
- Left-hand menus (Settings, Matchmaking, PvP Statistics, chat tab settings) keep their own look.

#### Bag pockets
- Each pocket is its own small tab standing on the Bag window, with a small gap between pockets.
- The selected pocket is wider and pops up 5px above the others. Hover makes a pocket lighter.
- Pocket icons sit centred. The Bag window, title and search box stay exactly where the game puts them.

#### Progress bars
- Every bar is a rounded dark track with a faint edge and a flat rounded fill, instead of thin striped lines.
- Where: Pokédex totals (Seen, Owned…), Pokédex base stats, Summary EXP / HP / happiness / contest stats, party and PC bars, request countdowns, matchmaking and the contest love meter.
- A value of 0 shows an empty track, with no leftover dot.
- The HUD event bars (wisps, raids) keep their look.

#### Trainer card
- The card has its own PokeMMO wordmark: "Poke" in the Titles colour and "MMO" in the Trainer card logo colour, which is your Accent by default.
- The wordmark is centred over the "Issued" date.
- The Accent line dips in a smooth curve under the date, and the date sits on a soft band (new option: Trainer card date band).

#### Login screen
- The PokeMMO logo sits 36px higher.
- Soft, shiny 4-point sparkles twinkle around the emblem. Each one has its own timing, they fade in and out gently, and they stay clear of the login window, logo, announcements and side buttons.
- New option: Login sparkles. By default it is your Accent mixed with white.

#### Pokémon Summary
- The grey top bar is dark blue and has its own colour (Pokemon Summary header).
- The value boxes on every page (overview, stats, IVs, Information, Particles) are flat rounded tiles with a faint edge, instead of bevelled boxes (Pokemon Summary boxes).
- The whole window body follows a new option, Pokemon Summary window.
- The Item Held bar is darker (Pokemon Summary item bar). "Item Held" and the item slot sit on matching raised tiles, and the item name is bold.

#### Contest screen
- It matches battle: theme buttons with properly centred text, battle-style top and bottom bands, the opponent box in the battle panel style, and the rounded love meter (Muted text colour, with gains in Accent).

#### Berry water tags (Better Water Levels – Fancy by Pancho412)
- Same Fancy shapes and positions, recoloured to the theme: dark tag with a faint edge, full drops in the new Berry water colour, empty drops dark, dry = red (HP bar – critical), and fully watered = a water-coloured tag with white drops.

#### Smaller touches
- HUD notification badge (new mail etc.): now the Accent colour (option: Notification badge) instead of fixed red.
- Matchmaking statistics: the tier tabs use the theme's buttons.
- Pokédex: the grid outlines (caught, caught OT, alpha, shiny, costume) and the matching totals bars share one colour each, all customizable.
- Symbol glyphs (GTL clear / refresh, arrows) follow the Text colour.

### Bigger buttons and windows
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

### Fixes
- **Battle HP bar at 0 HP:** it's empty now, with no red dot.
- **Battle move buttons:** they're no longer squashed the first time you open Fight.
- **Progress bars at 0** (e.g. contest stats): they no longer show a dot.

### Themes
- **"Better Default + Type Chart" removed:** the type chart is part of the main theme now. Point the mouse at your trainer name on the trainer card and the chart appears below the card. It covers all 17 types with Gen 2–5 rules. If you used the Type Chart theme, pick "Better Default" again.
- **New "Better Default (no battle backdrop)":** the same theme without the dark band behind the battle buttons and messages.

### Options: 56, was 36
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

### Tried and dropped during testing (not in the release)
- Separate "Type Chart" option and click-to-show type chart (hover on your name is what works).
- Battle backdrop colour option (didn't apply in game).
- Chat channel colour options (the game has its own chat colour settings).
- Hyper's encounter counter support (they restyle the old counter window; the new HUD counter replaces it).
- New bar style for the HUD wisp / event bars (not needed).

### Under the hood (for GitHub)
- **New textures:**
  - `res/bd-ui-111.png`: bar track and fill, trainer card band and dipping line, card wordmark.
  - `res/bd-water.png`: berry water masks.
  - `res/bd-sparkle.png`: login sparkles.
- **New files:**
  - `typechart.xml`: type chart on hover.
  - `no-backdrop.xml` and the `better-default-nobackdrop` theme entry.
- **Removed:** the `better-default-typechart` theme entry.
- **Changed textures:** `monster-info.png` (Summary header made tintable) and `bd-battle-extra.png` (HP bar with no dot at 0).
- **Copies of the game's own themes in `main-widgets.xml`.** They load last, so they replace the game's versions, and need refreshing if a game update changes them:
  - `broker-window`, `battle-frame`, `battle-panel`, `monster-frame`, `settings-colorselector`
  - `mods-panel`, `rom-panel`, `settings-panel`
  - `label-area-monsterdex`, `monsterdex-frame`, `monsterframe-progressbar-contest-2/total`
  - `inventory-tabbedframe`, `inventory-tab-empty`
  - `seed-plant-dialog`, `matchmakingframe`, `matchmaking-stats-frame`, `chat-tab-settings`
  - `contest-button`
- **`init.xml`:** tab rows (`base-tabbed-pane` and the generic `tabbedpane`) and bigger Yes / No buttons (`confirm-panel`).
- **New fonts:** `bd-tab` (tab text) and `bd-symbols-large` (GTL symbols).
- **Fonts now driven by options:** `battle` (Battle messages text), `main-lightgreen` / `pb-dark-green` (Good values), `main-red` / `pb-dark-red` (Bad values), and `symbols-white` (Text).
