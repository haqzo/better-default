# Better Default mobile compatibility — recovered development history

Historical research from owner development notes dated 12–16 November 2026. Current public release documentation is authoritative for 1.8.0. This record preserves the tested progression and failure lessons, not a proposal to reintroduce abandoned features.

## Build chronology

| Build | Evidence / result |
|---|---|
| 1.7.5 Test 6 | Owner-confirmed Android fallback, 75 settings. |
| Test 7 | Theme load failure after settings cleanup, new image constants and battle atlas changes. Cause not proven. |
| Tests 9/10 | Conservative rebuild from Test 6, 67 mobile settings and 13 presets; owner screenshots showed working Android UI but crowded effectiveness labels. |
| Test 11 | Static checks passed but runtime load failed after four new settings and image/widget changes. |
| Test 12 | Recovery from Test 10. Separate Badges-only fallback; later video confirmed Badges variant. Full variant was accepted as beta candidate, not independently proven by that video. |
| Test 13 / Full | Owner confirmed both load. 3× effectiveness sprite artwork with original logical sizes; Full retains patterned Summary cards. |
| Test 14 | Owner-confirmed Android build; stable Better Default (Mobile Beta) name and mobile-specific linear-filtered type atlas; released as 1.7.5 Mobile Beta. |
| 1.7.6 Tests 2–3 | Android .zip imports and PC-style Battle backdrop works. Phone-only theme entry removes not-a-mobile-theme warning. |
| 1.8.0 | Historical PC Test 7 and phone Test 5 approved by owner as final bases; PC and mobile changes distinct. Mobile Type Chart attempt dropped after load error (CONSTANT vs IMAGE mismatch). |

## Compatibility and theme architecture

- The theme package is ZIP-format; contents at archive root, not an enclosing directory. Maintain the correct mobile entry in info.xml. The later one-file mobile policy is Android and iPhone/iPad .zip with **only mobile theme registration**; retain shared PC resources used by includes. Do not select or register an unnecessary desktop entry on phone.
- Historical iPhone report: import failed with zip END header not found for the .mod, although local Java ZIP check passed. Extension handling was suspected, not proved. Android .zip import confirmed; iPhone/iPad runtime remains to be confirmed.
- Keep sequential image declaration/load order valid. Do not reference an image from a constant before it exists, and use correct option types (IMAGE vs CONSTANT). Avoid nested self-referencing widget overrides. Test 7/11 failed after multiple concurrent changes; no Mods Log was available to prove exact root cause. Isolate changes in a known-working baseline.
- Keep native touch hitboxes, widget sizing and game-controlled positioning intact. Visual offsets can be achieved through transparent padding; do not assume arbitrary relocation of the touch pad, battle hotbar, or native popups.
- Preserve desktop resources when doing a mobile-only pass (76 PC files in the historical 1.7.0 baseline were byte-verified). Use the actual version-matched desktop base for future changes, not necessarily 1.7.0.

## Relevant files

Within themes/better-default-mobile/: theme.xml (include order), options-mobile.xml (settings), android-widgets.xml (Summary/native widgets), battle-widgets.xml (move controls), gfx-mobile.xml (effectiveness), gfx.xml (Summary art), main-widgets-mobile.xml, hud-widgets-mobile.xml, android-shop-bd.xml. Review current package before assuming the historical layout persists.

Effectiveness: preserve all five labels (Status, Effective, Super effective, Not very effective, Immune) and dynamic colours. The proven Test 13 approach used 384×384 artwork (3× former 128×128) for en/es/fr/zh, bdm-eff-kit.png 312×180 (3× 104×60), area coordinates scaled 3× with sizeOverwriteH=104 and sizeOverwriteV=18. Visible label raised with transparent padding; game widget unchanged. Preserve localization, preset color constants, logical dimensions and left/right column spacing.

Summary cards: historical 260×80 native cards, patterned art with mn-sumbox and live accent colors; retain PP/type tags, normal/selected states and native star controls. No unapproved extra options.

Atlas: Test 14 kept the PC main.atlas/main.png unchanged and used separate mobile.atlas. 455 regions: 182 on original Nearest page, 273 skill_type_*, monster_type_* and skill_damage_* regions on 512×1024 mobile-types.png (2px padding, Linear). Region pixels, sizes and names verified unchanged. A 2× sprite diagnostic drew tags twice as large, so do not simply upscale the sprite's physical dimensions to improve sharpness.

## QA and reproducibility

Recovered tool notes: Python 3/Pillow (some NumPy), refcheck.py (undefined references/load order against version-matched game theme), optaudit.py (settings/preset values), ZipCheck.java (Java ZIP compatibility), mobile tools/pack.py (reference ZIP order/directory entries/compression); make_eff_hd.py and make_mobile_atlas.py for historical art workflow. Some scripts used session-specific paths; inspect and adapt before running. Tools themselves are not added by this note.

Validate ZIP integrity, XML parsing, image bounds and references, atlas region mapping, all 13 presets, PC byte equality for mobile-only work. Then actual client smoke: import, theme selection, restart, login/HUD, both move columns/all five effectiveness states, Summary Moves normal/selected, PP/type labels, Bag, GTL, Pokédex, popups and Gift Shop when relevant; alternate presets. Distinguish static checks from actual owner/device evidence. If load fails obtain Open Mods Log and isolate the smallest change.

## 1.8.0 owner decisions

Keep 13 presets, PC customization counts per current README, stable Mobile Beta name and one mobile file. Approved status style A, accent cursor style B, trainer header and stat bars; Type Chart Always show instead of unsupported click-to-stay-open. Title divider removed by owner; do not re-add without approval. Other rejected/deferred ideas: Summary tab tiles, server status restyle, Base Stats rows, Egg Incubator redesign. Left battle-column nudge, unresolved Summary sliver control, iPhone confirmation and Gift Shop special-label screenshot are historical open checks, not approved implementation tasks.

Source: recovered Better Default 1.8.0 dev notes, mobile README, Tests 9–14 notes, technical map, status/roadmap and dev tool README. Official example format: https://github.com/PokeMMO/PokeMMO_Mods/tree/master/examples. Original notes and test artifacts remain in private storage; no client dumps or personal screenshots published.
