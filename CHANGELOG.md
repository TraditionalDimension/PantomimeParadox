# Changelog — Pantomime Paradox

## v1.5.3 - 2026-04-01 - Fix patch

### Fixed
- Fixed additional issues with **Every Ante Task Mode** exact-card discard objectives not always registering correctly.
- Fixed cases where discarding a targeted card together with other cards could fail to complete the objective.
- Fixed edge cases where exact-card discard tracking could miss real discard actions depending on the hook path used.

### Changed
- Improved **Every Ante Task Mode** objective tracking for exact-card discard tasks.
- Exact-card discard objectives are now handled more robustly across different discard flows.
- Added safer matching logic for targeted discard objectives to better handle edge cases.

### Compatibility
- Improved task text generation for card-based objectives that reference:
  - Editions
  - Seals
  - Enhancements
- Objective text now resolves **real localized names** more reliably instead of showing raw internal keys.
- Improved compatibility for modded card properties when they are registered through standard localization/center data.
- Vanilla card properties such as **Foil**, **Holographic**, **Polychrome**, and other standard labels now display correctly in Every Ante card objectives.

## v1.5.2 - 2026-03-31 - Fix patch

### Fixed
- Fixed a bug where buying a **Voucher** did not count toward Task Mode objectives.
- Fixed a crash in **Every Ante Task Mode** caused by invalid sorting during dynamic task generation.

### Changed
- Reworked **Every Ante Task Mode** to generate tasks more dynamically instead of relying only on a rigid seeded cycle.
- Every Ante tasks can now take the current deck state into account when selecting objectives.
- Added support for **specific-card objectives** in Every Ante mode:
  - Play a specific card
  - Discard a specific card
- Specific-card objectives now track the chosen playing card by its internal card identity instead of its current appearance, making task tracking more reliable.
- If a targeted card for an Every Ante objective is removed from the deck, the task is now regenerated automatically instead of becoming a dead objective.
- Added anti-repetition logic to reduce how often similar Every Ante tasks appear back-to-back.
- Expanded dynamic Every Ante task selection to better consider real deck properties, including:
  - Rank
  - Suit
  - Enhancement
  - Seal
  - Edition

### Localization
- Added **32 new failure lines** for Jimbo when losing due to unfinished Task Mode objectives.

## v1.5.1 - 2026-03-30 - Feature + Fix patch

### Added
- Added **Every Ante Variant** for Task Mode.
- Added new Task Mode objectives for:
  - playing filtered cards
  - discarding filtered cards
  - activating Boss Blinds multiple times
- Added task-pool filtering based on whether the mod's main content is enabled.
- Added per-run seeded task ordering for **Every Ante Variant**, so ante task scenarios now vary between runs while staying stable within the same run.

### Changed
- Reworked Task Mode flow so the start-run menu now shows only one Task Mode toggle at a time, based on config settings.
- Updated config behavior for Task Mode / Every Ante Variant to make setup clearer and easier to understand.
- Moved the **Every Ante** config toggle to the second config column to prevent layout overflow.
- Improved Every Ante task generation and target handling to make runs less repetitive and more interesting.
- Refined Task Mode HUD drag handling so the visible task panel now matches its real draggable area.

### Fixed
- Fixed Task Mode HUD drag hitbox being offset from the visible task panel due to coordinate-space mismatch.
- Fixed Every Ante Variant crash caused by calling `task_seed_base` before its local definition was available.
- Fixed Every Ante Variant crash caused by invalid randomized sorting logic in seeded ante task ordering.
- Fixed repeated identical Every Ante task scenarios appearing across different runs.
- Fixed Task Mode UI/config inconsistencies related to Every Ante toggle presentation.

### Notes
- Task Mode for a full run still works as before.
- Every Ante Variant now functions as a distinct Task Mode style with proper seeded variation and corrected startup behavior.

## v1.5.0 - 2026-03-29 - Major Update

### Added
- Added **Task Mode** as a new optional run modifier.
- Added a **Task Mode toggle** to run setup.
- Added a config option to keep the **Task HUD visible by default**.
- Added a dedicated **Task HUD** that displays the active objective, live progress, completion state, and a final warning before the last Boss.
- Added a custom **Task Mode fail presentation** on defeat, including a Joker appearance and unique speech lines.
- Added support for new Task Mode objective types, including:
  - **Skip Blind**
  - **Reroll Shop**
- Added proper Task Mode text support for the newer objective categories instead of falling back to raw internal IDs.

### Changed
- Task Mode now properly reacts to **Hard Mode** and **Impossible Mode** at run start.
- Task targets now scale correctly for:
  - normal runs
  - Hard Mode runs
  - Impossible Mode runs
  - combined Hard + Impossible runs
- Most Task Mode objectives now receive a small per-run target variation to improve pacing and balance.
- The target variation range for most objectives was adjusted to **[-2; +7]**.
- **Score Chips in one hand** objectives are intentionally excluded from that variation.
- Task HUD default placement was adjusted.
- Task HUD generation and refresh flow were reworked to better handle dynamic objective text and post-layout sizing.
- Task fail timing was adjusted to better match vanilla-style defeat pacing.

### Balance Changes
- **Mime-Costumer** was rebalanced. Its scaling no longer grows directly with Ante value. It now uses a tiered ante bracket formula instead:
  - Ante 1–4 → x1
  - Ante 5–8 → x2
  - Ante 9–12 → x3
  - and so on
- **Mime-Witchess** was simplified and rebalanced:
  - it now pays out on the **first held card only**
  - **Magical edition** is no longer required
  - the effect is now more deterministic and easier to read
- **Acrylic Mime** is no longer Eternal-compatible.
- **Steel Mime** is no longer Eternal-compatible.

### Fixed
- Fixed Task Mode sometimes failing to detect Hard / Impossible mode toggles correctly at run start.
- Fixed **Skip Blind** objectives not registering correctly.
- Fixed **Reroll Shop** objectives not registering correctly.
- Fixed missing objective descriptions for newer Task Mode entries such as Blind skips and shop rerolls.
- Fixed several Task HUD initialization / refresh regressions that could cause startup crashes.
- Fixed Task HUD creation issues caused by local function ordering during initialization.
- Fixed Task Mode defeat overlay appearing without the Joker character and speech bubble.
- Fixed Task Mode fail speech flow by spawning the Joker manually and delaying the line similarly to vanilla game over behavior.
- Fixed several early HUD sizing / syncing issues that affected the draggable task board.

### Task Mode
Task Mode adds a single active objective to the run. The objective must be completed before the run ends.

Examples of supported objective families include:
- playing specific poker hands
- discarding specific poker hands
- buying or selling cards, packs, vouchers, and related content
- using Tarot, Planet, or Spectral cards
- destroying filtered cards
- skipping Blinds
- rerolling the shop
- reaching exact state-based thresholds
- scoring a required amount of Chips in one hand
- upgrading specific hand levels

Additional notes:
- Task Mode objectives now correctly scale with **Hard Mode** and **Impossible Mode**.
- Exact target values are not permanently locked and may still be tuned in future balance passes.
- Most task values can also receive a small generated variation per run for healthier balancing and less predictable pacing.
- The Task HUD is draggable, but the **currently reliable grab area is the upper-right corner of the board**.

### Known Limitation
- Task HUD dragging is functional, but practical grabbing is still limited to the **upper-right corner** for now.

### Balance Note
- Task Mode objective values are still considered balance-sensitive.
- Exact numbers may be raised or lowered in future updates if specific tasks prove too weak, too easy, too slow, or too punishing in real runs.

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
