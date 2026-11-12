# Better Default changelog

## 1.7.5 — Mobile Beta

### New: Better Default for phones and tablets (beta)
- A separate download, **`Better-Default-1.7.5-Mobile-Beta.mod`**, with the theme **Better Default (Mobile Beta)**.
- It is the game's own phone layout (big touch buttons, full-screen windows) in the Better Default design, with the same colours and the **same 13 presets** as on PC.
- Drawn for the phone in the same style:
  - **Full-screen windows** also fill the strip under the game area, so there is no black band at the bottom of the screen.
  - **Rounder corners** made for touch, and the new HUD's **line icons** for the phone buttons (close, settings, menu, chat, arrows…).
  - **Pokémon Summary:** tab buttons with icons — the open page is a bright tile with an Accent border, the other pages are faint. The move cards are dark with a subtle pattern and an Accent stripe; the selected move gets an Accent border. A small gap between the value boxes.
  - **Battle:** the move buttons are big type tags (type colour, soft gradient, type symbol). The effectiveness labels (**Super effective, Effective, Not very effective, Immune, Status**) are redrawn sharp in English, Spanish, French and Chinese and fit inside their pill. Round battle buttons with the HUD's icons. The battle Bag shows the item description on a panel.
  - Type and move tags are scaled smoothly on phones (the phone theme has its own copy of the sprite atlas).
  - Rounded checkboxes, the chat window in the **Chat background** colour, more padding on Gift Shop cards, and the **Fancy berry water drops** like on PC.
- **67 Theme Settings on phones (57 colours + 10 settings).** Only settings that change something on a phone are listed. Left out (PC-only): Bag height, Pokédex height, Battle backdrop, Encounter counter style and its three colours, Type chart, Pokémon Summary item bar. Window border and Window border width are called *(popups)* there, because they only show on popups and NPC dialogue.
- **Phone-only settings:** *Summary tabs: open page border* (Tab border accent / soft / off), *Summary tabs: other pages* (Other tabs faint / solid / icons only) and *Battle move buttons* (Moves bright / deeper / dark).
- Tested on Android. iPhone / iPad have not been tested yet.

### Known beta limits
- The movement pad, the battle item bar and some popups are placed by the game; a theme can't move them.
- Type and move tags can only be smoothed, not made sharper: the game draws them at their own pixel size on phones (tested).
- In the left battle column the type tag sits close to the button edge.
- After switching from another theme the game may show *"Could not load theme Better Default because it is not a mobile theme"* once — pick **Better Default (Mobile Beta)** in Settings → Interface → Theme and restart.

### PC
- No changes: the PC theme is the same as in 1.7.0 (only the version number and the README changed). If you already use 1.7.0 on PC, updating is optional.

### Under the hood
- The mobile `.mod` has two theme entries: **Better Default** (PC, `themes/better-default/`, byte-identical to 1.7.0) and **Better Default (Mobile Beta)** (`themes/better-default-mobile/`, built on the game's `data/themes/android` layout files).
- The phone entry uses its own sprite atlas, `custom-atlas/mobile.atlas` (the PC `main.png` page + a `mobile-types.png` page with the type / move / damage-class tags on smooth filtering). The PC entry still uses `custom-atlas/main.atlas`, unchanged.
- Effectiveness label sheets `res/effectivity_buttons_{en,es,fr,zh}.png` and `res/bdm-eff-kit.png` are drawn at 3× and shown at the game's size.
- Theme revision 11 (game update of 6 Nov 2026).

## 1.7.0 — type tags, window borders & new presets

### New type, move and damage-class tags
- Every type tag, move tag and damage-class tag (Physical / Special / Status) is redrawn, **in all seven languages the game has tag pictures for** (English, German, Spanish, French, Italian, Korean, Chinese).
- Title case in the theme's bold condensed font with a dark edge, the official type colours with a soft gradient, and a modern type symbol (flame, drop, leaf, bolt, snowflake, dragon scales…).
- **Pokémon Summary › Moves:** the move tag is as tall as the move box and sits right beside it; move names are centred in the box.

### New settings (Theme Settings)
- **Type chart:** *Show when hovering your name* or *Type chart off*.
- **Bag pockets:** how the selected pocket in the Bag's top row looks — *Pill*, *Underline*, *Underline, faint buttons*, *Underline only*, *Pill + underline*, *Accent ring* or *Accent ring + underline*. The underline sits under the pocket.
- **Window border:** *No window border*, *Faint*, *Medium* or *Strong*. The border is part of each window's own shape, so it follows every window exactly — also the type chart and the NPC dialogue box.
- **Window border width:** *Thin* or *Thick*.
- New colour **Window border colour** (every preset starts with its Accent).
- **73 options in total:** 61 colours + 12 settings. All 13 presets set every one of them.

### Presets
- **Two new presets:** **Catppuccin Mocha** and **Tokyo Night**, in the official colours of those popular themes. Catppuccin Mocha uses mauve as the Accent; Tokyo Night uses its green, with cyan links and a magenta trainer card logo and login sparkles.
- **Colours tuned so each preset matches its name:** PokeMMO Gold uses the game's own gold, Amethyst is a deeper purple, Emerald green (was mint), Sakura a softer pink, Ember more orange, Crimson a deeper red, and **OLED Black has true black windows**.
- Press **Apply Theme Preset** to load the new values.

### Icons
- The small interface icons (settings gear, trash, lock, pin, sort, sound, select all, edit, close, help, rotate) are redrawn as clean flat icons.
- The little pixel pictures (BP, coins, clock, seasons, shiny stars, alpha, hordes, map, dice, status icons…) get the cleaner Better Items look.
- Icons and tags only change while Better Default is the selected theme.

### Look and fixes
- **Login screen:** the PokeMMO logo uses the same bold condensed font as the tags, with a thin dark edge so it stays readable over the bright login scene.
- **Bag:** the pocket row is taller, so the pocket icons sit centred in their buttons.
- **Pokémon Summary:** 4px wider, so the bigger shiny star, alpha and hidden ability badges fit. The Item Held tile is centred on the item and has the same height as the Item Held bar.
- **GTL:** item icons in the tables sit on the same tile as the Bag slots (with the faint cell edge), so dark icons no longer fade into the row.
- **Poké Mart:** item names stop before the icon instead of running under it (a very long name shrinks a little and ends in "…").

### Under the hood
- Own sprite atlas: `custom-atlas/main.atlas` + `main.png` (1024×1024), chosen with `sprite_atlas` on the theme entry in `info.xml`, so the tags and icons only apply to Better Default. It is a full copy of the game's `sprites/atlas/main.atlas` — refresh it if a game update changes that atlas. Move tags (`skill_type_*`) are 50×36 regions.
- New image `res/bd-170-border.png` (window border rings). New settings in `info.xml`: Type chart, Bag pockets (IMAGE), Window border, Window border width (CONSTANT, values in `options.xml`).
- Copies of game themes (refresh them if a game update changes them), in `main-widgets.xml`: `broker-table` (GTL icon cell), `market-button` (Poké Mart rows), `label-monster-area` (Summary move labels).
- Theme revision 11 (game update of 6 Nov 2026).

## 1.6.5 — one theme, settings instead of versions

### No more theme versions: Battle backdrop and Login screen are now settings
- **Battle backdrop** and **Login screen** are now part of the default theme. They are dropdowns in **Settings › Interface › Theme Settings**, so there is only **one theme: "Better Default"**.
- The versions **"Better Default (no backdrop)"**, **"Better Default (game login)"** and **"Better Default (no backdrop, game login)"** are **gone**. If you used one of them, pick **"Better Default"** again and set the two dropdowns:
  - **Battle backdrop:** *Battle band* (the dark band behind the battle buttons and messages) or *No backdrop*.
  - **Login screen:** *Better Default backdrop*, *Better Default backdrop (no sparkles)* or *Game login scene* (the game's own animated login scene; avoids the one-frame flash when you enter the game, like the old "game login" versions).
- Press **Apply Theme Preset** once after updating, so every new setting gets its value.

### New settings (Theme Settings)
- **Encounter counter style:** *Accent line* (new) or *Plain panel*.
- **Bag height:** 378 (game) / 518 / 658. **Pokédex height:** 250 (game) / 390 / 530.
- **Selection ring:** bold / normal / soft / off — the ring on the selected tab, bag pocket and tile.
- **Selected highlight:** strong / normal / soft — the fill on selected rows, tabs and tiles.
- **Edges:** bold / normal / soft / off — the faint outline on windows, panels, tabs, buttons and boxes.
- New colour option **Encounter accent** (every preset sets it to its Accent).
- **68 options in total:** 60 colours + 8 settings. All 11 presets set every one of them.

### Look
- **Bag:** one window. The pocket row now sits inside the bag window; the selected pocket is a raised pill with a clearer focus ring.
- **Encounter counter** (small and big): an accent line along the top, so it matches the rest of the HUD.
- **Login announcements** (bottom left): the theme's rounded buttons with a small gap between them.
- **Battle stat labels** (+2 Atk / −1 SpA): back to the outlined look from before the game update.

### Spacing and fixes
- **− value +** rows (Settings, GTL, shops…): a small gap between the buttons and the value.
- **Dropdown lists:** a 2px gap between the hovered row and the selected row.
- **GTL Item Market:** bigger − / + / Buy / Cancel buttons with gaps between them, and a bigger refresh button.
- **GTL purchase confirm** ("Are you sure you wish to purchase that listing?"): a gap between the sprite tile and the name box.
- **PC preview:** the rounded corners are cut out cleanly (no more ghost squares on type-tinted previews).

### Under the hood
- One theme folder (`themes/better-default/`); `no-backdrop.xml`, `default-login.xml` and the three version folders are removed.
- New `options.xml` (values for the new settings, loaded first). Battle backdrop, Login screen and Encounter style are IMAGE settings, Bag / Pokédex height INT, Selection ring / Selected highlight / Edges CONSTANT (they set the strength of the ring, highlight and edge images).
- Copies of game themes (refresh them if a game update changes them): in `main-widgets.xml` `label-settings-vai` (Settings value rows) and the previous `stat-boost` / `stat-drop`; changed in `main-widgets.xml` `logingui`, `changelog-frame`, `battle-frame` / `battle-panel`; changed in `init.xml` `confirm-panel` › `container` (gaps), `gtl-buy-panel`, `valueadjuster`.
- Theme revision 11 (game update of 6 Nov 2026).

## 1.6.0 — new game default + polish

- **Fixed after the game update:** The theme is rebuilt on the game's new default theme (new fonts, HUD fonts, HUD atlas and widgets, mail reward slot), so it **loads again** with the current client.
- **Login:** The side menu buttons (Repair Client … Exit) have a 4px gap, no more doubled edges.
- **Settings:** Settings > Other: narrower value columns so every column fits in the window.
- **Gift Shop:** Buy buttons on the sprite cards (Specials, Vanity Items …) are the same size as the other cards.
- **Pokémon Summary:** Rounded window with the theme's faint edge, like every other window. The Pokémon display is its own rounded box with a soft rim, sitting in one panel with the Item bar.
- **PC Deposit Box:** The window content sits 10px lower, so it no longer runs into the title bar; rounded corners and a faint border.
- **Battle bag:** 4px gap between the item rows.
- **GTL:** Slightly bigger page buttons (<< 1 2 3 … >>).

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
