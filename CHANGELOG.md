# Changelog — Pantomime Paradox

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
