MeiShi Card Viewer
====================

Open index.html in a modern browser.

Media support:
- 149 separated, translated mouse SWF files under assets/ruffle_mice
- 149 mouse catalog entries have exact-ID animation matches
- 134 map background files under assets/bgs
- 95 map entries have matched backgrounds

Exact mouse ID rule:
- A mouse only uses a SWF whose filename starts with that same mouse ID.
- No ID rewriting or fallback is performed.
- Example: mouse 0x0034 uses 0x0034_-_Orange_Skateboard_Rat.swf.
- A 0x1xxx SWF is only used when the mouse entry itself has that exact 0x1xxx ID.

Translated SWF layout:
- The folder separation from mice.zip is preserved (land, air, in_water, seabed, and so on).
- The viewer displays the translated SWF name in the animation section.
- SWF bytes are also embedded in assets/mouse_swf_data.js so animations can load from a directly opened index.html.

Ruffle is loaded from its official unpkg package, so an internet connection is still needed for the Ruffle emulator itself. Cards, XML data, searches, filters, map backgrounds, and the bundled SWF files remain local.

Ruffle sizing:
- Mouse animation details use a wide 4:3 player area.
- Ruffle uses exactFit so the SWF stage fills the player.

Level Maker
-----------
- New Level Maker tab with 876 templates from four MapMouse XML files.
- Edit map metadata, bosses, default cards, mouse roster, per-mouse coordinate strings, and both drop lists.
- Load templates, import XML, validate, copy/download one item, or build and export a complete MapMouse.xml level set.
- Draft level sets are saved in browser localStorage.
- Original XML files are included under assets/level_templates.
- Mouse IDs are never rewritten; exact IDs are exported.

Roster, animation, and CDN update
---------------------------------
- Map detail pages now show the exact MapMouse enemy roster for the matching level template.
- Each roster entry includes the mouse name, exact ID, type, HP, speed, SWF availability, and both coordinate strings.
- Clicking a known roster mouse opens its full mouse detail and Ruffle animation.
- Level Maker mouse rows are visual, draggable, touch-friendly, and keep MouseID, MousePoint, and MouseGamePoint aligned.
- Level Maker card and mouse rows include quick viewer/CDN buttons.
- Ruffle details now include pause/play, restart, timeline speed, zoom, background, and fullscreen controls.
- Card details include both q.ms.huanlecdn image URL patterns.
- Mouse details include the q.ms.huanlecdn exact-ID SWF URL.
- Map CDN links remain unconfigured until the map URL pattern is known.
- An empty .nojekyll file is included so GitHub Pages serves the literal #Uxxxx background filenames.

Card PNG update
---------------
- Added 61 additional exact-ID card PNGs under assets/cards.
- The viewer now recognizes 1030 card IDs with local artwork.
- Card search, map recommendations, and Level Maker selectors use the new artwork automatically.
