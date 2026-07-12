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
