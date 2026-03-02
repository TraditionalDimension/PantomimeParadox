# Changelog — Pantomime Paradox

## v1.4.0 - 2026-03-02
### New Jokers
- Mime-Couplet
- Mime-Costumer
- Mime-Monopolist
- Mime-Mystery
- Mime-Alchemist
- Mime-Witchess
- Mime-Wizard
- Mime-Master Planetarium
- Mime of Kings
- Mime of Queens

### Fixes / Changes
- Baron Mime: ante-dependent behavior updates during gameplay (not only tooltip refresh).
- Function that need for finding correctly Most Played Hand: defaults to High Card when all hands are 0; deterministic tie-breaking.
- Consumeable spawning: added TDPP_can_add_consumeable() and updated related jokers to respect consumeable_buffer (prevents overflow with Purple Seal and similar).

## 1.3.2 - 2026-02-18
### Fixed
- **Magical Edition**: restored the **apply SFX** and the **juice/bounce animation** on edition application (now matches vanilla Foil/Holo/Polychrome behavior).
- Fixed cases where Magical Edition was not react to Glass Cards.

### Masked Packs
- Add **pre-show Jokers** pause for packs. If this option is enabled in the mod’s config menu, the game will wait one second after opening the pack before shuffling the Jokers to determine its contents.
- Minor pack text/logic tweaks fix for clearer and more consistent results.


## 1.3.1
### Added / Updated
- Config menu layout: multiple columns for better readability.
- New optional vanilla Joker scaling buffs (each has its own toggle):
  - Misprint (max by Ante)
  - Hiker (by Ante)
  - Suit Jokers (by Ante)
  - Hand Jokers (base scaling by Ante)
  - Half Joker (by Ante)
  - Banner (by Round)
  - Mystic Summit (by Ante)
  - Additional optional buffs (Scary Face, Fibonacci, Scholar, Abstract, Even Steven, Odd Todd, To Do List, Smiley Face, Walkie Talkie, Castle, Rough Gem, Arrowhead, Onyx Agate, Bootstraps, Bull, Runner)
  - Splash: optional 5-card bonus chips in scoring context
- New Run UI: improved injection logic so toggles can **merge** with other UI mods (e.g. Partner / Galdur Compat).
- Main content master toggle (separate from the columns): enables/disables main mod content (**restart required**).

### Fixes
- Magical Edition tag gain sound behavior adjusted (uses the same sound approach as Boon).
