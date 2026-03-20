# Changelog — Pantomime Paradox

## v1.4.3 - 2026-03-20 - Major Balance Update

### Balance Changes

- **Synthy Mime**
  - Moved to **Rare**
  - Maximum effect simplified to **1 retrigger**

- **Thief Mime**
  - Chance improved from **1 in 3** to **1 in 2**

- **Glass Lucy**
  - Now retriggers eligible cards **1** additional time

- **Miner Mime**
  - Now retriggers eligible cards **1** additional time

- **Ghosty Mime**
  - Now retriggers eligible cards **1** additional time

- **Mime of Hearts / Clubs / Spades / Diamonds**
  - Cost increased to **$12**

- **Mime Couplet**
  - Moved to **Common**
  - Cost changed to **$7**

- **Mime Engineer**
  - Reduced from **X1.25** to **X1.15**

- **Ancient Enlightenment**
  - Reduced from **+3** to **+2**

- **Seventh Mime**
  - Moved to **Uncommon**

- **Banker Mime**
  - Chance reduced from **55%** to **35%**
  - Cost increased to **$12**

### Reworks

- **Leprechaun Mime**
  - Reworked into a simple retrigger effect for played and held in hand **Lucky** cards

- **Mimetinum Lady**
  - Reworked into a simple retrigger effect for played and held in hand **Platinum** cards

- **Baron Mime**
  - Now grants bonus only from **held in hand** face cards
  - Its scaling now increases only from discards made up entirely of **face cards**

- **Glass Mime**
  - Removed the extra **Chips** gain from Glass cards
  - Now has a **1 in 4** chance to destroy itself at end of round

- **Moneylender Mime**
  - Reworked completely
  - Now adds a random **Gold** or **Platinum** playing card with a **Gold Seal** at the start of round
  - Now supports **Blueprint**

- **Sixth Mime**
  - Reworked completely
  - Moved to **Uncommon**
  - Each held in hand **6** now has a **1 in 6** chance to create a random **Spectral** card

### Other Changes

- **Faded Seal**
  - Bonus variance changed to **-6% to +6%**

- **Acrylique Mime**
  - Cost increased to **$12**
  - Now has a **1 in 3** chance to destroy itself after each hand

- **Steel Mime**
  - Cost increased to **$12**
  - Now has a **1 in 2** chance to destroy itself after each hand

- **Charlie Mime**
  - Now only reacts to the **first discard** each round

## v1.4.2 - 2026-03-03 - Hotfix

### Fixes
- **Master Planetarium**: now correctly triggers **each round** on the **first hand** when it contains **4+ cards of the same rank**. Works properly with **Blueprint/Brainstorm**.

## v1.4.1 - 2026-03-03
### Added
- 3 new Challenges:
  - Fishing with Wife
  - Queens Order
  - Tired Rulers

### Fixes / Changes
- Boss Blinds: effects now properly stop after selling **Luchador** (disabled boss no longer triggers on the next hand).
- Fix some arts.

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
