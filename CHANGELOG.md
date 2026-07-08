# Changelog — Pantomime Paradox

## 1.13.0 - 2026-07-08 - Double Act Update

### New Jokers

Added 31 new Jokers focused on transformation, Tags, poker-hand progression, playing-card creation, and XMult scaling.

#### Double Act Family

Added Double Act and 5 Jokers that can transform into it.

* Added Double Act.

  * At end of round, checks whether remaining Hands, remaining Discards, and the last digit of current money are equal.
  * When the condition is met, becomes a full copy of the leftmost other Joker.
  * The equality check happens before Gold Cards pay out.
  * Not Blueprint compatible.
* Added Casting Call.

  * Each shop Reroll has a 1 in 3 chance to become Double Act.
* Added Outtake.

  * Each discard has a 1 in 5 chance to become Double Act.
* Added Cue Card.

  * Each played hand has a 1 in 5 chance to become Double Act.
* Added Receipt.

  * Each card purchase has a 1 in 5 chance to become Double Act.
* Added Stage Prop.

  * Each Consumable use has a 1 in 5 chance to become Double Act.

All 6 transformation paths now use a step-by-step flip, transform, and reveal animation.

#### Equality and Target Mimes

Added 4 Mimes built around resource equality and card targeting.

* Added Juliette Mime.

  * Before each played hand or discard, checks whether remaining Hands and Discards are equal.
  * When the condition is met, creates The Emperor if there is room.
  * Blueprint compatible.
* Added Livia Mime.

  * Before each played hand or discard, checks whether remaining Hands and Discards are equal.
  * When the condition is met, levels up a random visible poker hand.
  * Blueprint compatible.
* Added Mireille Mime.

  * Before each discard, checks whether remaining Hands equal the last digit of current money.
  * When the condition is met, destroys the rightmost card held in hand and earns $7.
  * Blueprint copies the money reward without duplicating the destruction.
* Added Katarina Mime.

  * At start of round, selects a rank and suit from the full deck.
  * Destroying matching cards creates one random non-Boss Tag for each matching card destroyed.
  * Blueprint compatible.

#### Random Tag Mimes

Added 6 Mimes that can create random non-Boss Tags.

* Added Nadine Mime.

  * Opening a Booster Pack has a 1 in 4 chance to create a random Tag.
* Added Odette Mime.

  * Skipping a Booster Pack has a 1 in 2 chance to create a random Tag.
* Added Rosalie Mime.

  * Each shop Reroll has a 1 in 4 chance to create a random Tag.
* Added Sabine Mime.

  * Each discard has a 1 in 4 chance to create a random Tag.
* Added Thalia Mime.

  * Each Consumable use has a 1 in 5 chance to create a random Tag.
* Added Vivienne Mime.

  * Selling a card has a 1 in 4 chance to create a random Tag.

All random Tag effects exclude Boss Tags and use queued popup, card-juice, Tag creation, and sound feedback based on Woman Mime's presentation flow.

#### Poker-Hand and Orbital Mimes

Added 7 Mimes focused on hand levels and Orbital Tags.

* Added Ophelia Mime.

  * Each trigger of a played card has a 1 in 6 chance to level up a random visible poker hand.
  * Blueprint compatible.
* Added Penelope Mime.

  * Each trigger or retrigger of the first card held in hand has a 1 in 3 chance to level up a random visible poker hand.
  * Blueprint compatible.
* Added Aurelia Mime.

  * Each played hand has a 1 in 3 chance to create an Orbital Tag for a random visible poker hand.
  * Blueprint compatible.
* Added Magnesia Mime.

  * Each discard has a 1 in 3 chance to create an Orbital Tag for a random visible poker hand.
  * Blueprint compatible.
* Added Quintessa Mime.

  * After each shop Reroll, has a 1 in 2 chance to level up Flush Five.
  * If Flush Five is hidden, levels a random visible poker hand instead.
  * With Space Joker present, has a separate 1 in 3 chance to create an Orbital Tag for the actual hand selected by the effect.
  * Blueprint compatible.
* Added Seraphine Mime.

  * After each shop Reroll, has a 1 in 2 chance to level up Flush House.
  * If Flush House is hidden, levels a random visible poker hand instead.
  * With Space Joker present, has a separate 1 in 3 chance to create an Orbital Tag for the actual hand selected by the effect.
  * Blueprint compatible.
* Added Valeria Mime.

  * After each shop Reroll, has a 1 in 2 chance to level up Five of a Kind.
  * If Five of a Kind is hidden, levels a random visible poker hand instead.
  * With Space Joker present, has a separate 1 in 3 chance to create an Orbital Tag for the actual hand selected by the effect.
  * Blueprint compatible.

The new Orbital Tag flow now waits for hand-level feedback before showing the Tag popup and creating the Tag.

#### Boss Blind Card Creators

Added 3 Jokers that create playing cards during Boss Blinds.

* Added Refine.

  * Each discard during a Boss Blind creates a random Enhanced playing card.
  * Blueprint compatible.
* Added Imprint.

  * Each discard during a Boss Blind creates a random playing card with a random Edition.
  * Blueprint compatible.
* Added Stamp.

  * Each discard during a Boss Blind creates a random playing card with a random Seal.
  * Blueprint compatible.

#### XMult Jokers

Added 5 new XMult Jokers.

* Added Altered Deck.

  * Starts at X1 Mult.
  * Gains X0.23 Mult for each Enhanced card in the full deck.
* Added Marked Deck.

  * Starts at X1 Mult.
  * Gains X0.23 Mult for each card with a Seal in the full deck.
* Added Printed Deck.

  * Starts at X1 Mult.
  * Gains X0.23 Mult for each card with an Edition in the full deck.
* Added Patron's Aura.

  * Starts at X1 Mult.
  * Gains X0.5 Mult for every Voucher redeemed during the current run.
  * Correctly counts Vouchers redeemed before Patron's Aura was obtained.
* Added Consumption.

  * Starts at X1 Mult.
  * Permanently gains X0.17 Mult whenever a Consumable is used.
  * Blueprint copies the payout without duplicating the stored gain.

### Deck and Sleeve Changes

Updated Coral Deck.

* Coral Deck now also starts with 2 Judgement cards.

Updated Acid Deck and Acid Sleeve.

* Oxidation no longer attempts to trigger after every played hand and every discard.
* Oxidation now triggers only on the first played hand and the first discard of each round.
* The played-hand and discard triggers are tracked separately, allowing at most one trigger of each type per round.
* CardSleeves descriptions were updated to match the new behavior.

### Existing Joker Changes

Updated Fifth Mime.

* Reworked the effect.
* Each played or held 5 now gives +50 Chips.
* Removed the previous Consumable-count scaling effect.

Updated Mime of Aces.

* Reworked the effect.
* Each played or held Ace now gives +5 Mult.
* Removed the previous Straight / held-Ace / Strength-generation effect.
* Cost reduced from $7 to $5.

Updated Baron Mime.

* Now starts at +1 Mult.
* Its stored Mult can no longer fall below +1.

Updated Curator Violet.

* Its total multiplier now has a minimum of X1.5.

Updated Emerald Mime.

* Rarity changed from Rare to Uncommon.
* Cost reduced from $12 to $8.

Updated Mime Gambler.

* Still creates a Standard Tag every 3 shop Rerolls.
* Now also creates The Hanged Man when there is Consumable room.

Updated Mime Agony.

* Added a new end-of-round equality bonus.
* If remaining Hands, remaining Discards, and the last digit of money are equal, may create a Luchador if there is room.
* The original Joker and each Blueprint source can resolve their own Luchador creation.
* Existing scoring and growth / decay behavior is preserved.

Updated Jester Mime.

* Still creates The Soul after 21 shop Rerolls.
* Now also has a 25% chance to create an Abyssal Tag.

Updated Uncommon Mime.

* Tag reward changed to 80% Uncommon Tag / 20% Abyssal Tag.

Updated Rare Mime.

* Tag reward changed to 75% Rare Tag / 25% Abyssal Tag.

Updated Spectral Mime.

* Tag reward changed to 55% Ethereal Tag / 45% Abyssal Tag.

Updated Spectral Shard.

* Corrected displayed variables and text for its negative-to-positive money range.

Updated Albert Mimestein.

* Improved scoring-value detection when face-down-card situations hide or temporarily zero normal HUD hand values.
* Uses live scoring Chips and scoring-hand fallbacks when needed.

### Shift Rerolls

Expanded Shift Reroll economy and shop compatibility.

* Added a configurable price increase per Shift Reroll.

  * Range: $1 to $10.
  * Default: $4.
  * The first Shift Reroll remains free.
  * With the default setting, costs progress as Free -> $4 -> $8 -> $12 and so on.
* The selected price increase is locked in when a new run starts.
* Improved shop-row replacement.

  * Unsupported or empty shop slots now fall back to normal shop-card generation.
  * Partially unsupported shop rows can still be shifted.
  * Shift cost and usage statistics are applied only after a successful row replacement.
* Added selected-card preview to the Shift Reroll List.

  * List rows can be clicked or confirmed to preview their card.
  * Added safer preview failure handling.
* Improved controller and gamepad navigation for the Shift Reroll List.
* Added localization for the new Shift Reroll economy and behavior settings.

### Blueprint and Trigger Fixes

Fixed Monochrome Mime with Blueprint and other copying effects.

* Blueprint now correctly copies Monochrome Mime's response to a successfully triggered Tag.
* Duplicate-trigger protection now works without depending on the copying Joker having an `ability.extra` table.

Fixed Livia Mime and Juliette Mime.

* Their equality condition now compares only remaining Hands and remaining Discards.
* The last digit of money is no longer part of their condition.
* Mime Agony and Double Act still use the three-way Hands = Discards = money-digit condition.
* Mireille Mime still uses Hands = money-digit.

Fixed Vivienne Mime.

* Base chance changed from 1 in 3 to 1 in 4.
* Gameplay, localization variables, and JokerDisplay now agree.

Improved new Tag-creation feedback.

* New 1.13 Tag creators now use ordered popup, juice, Tag creation, and sound events.
* Katarina Mime now shows one complete feedback sequence for each Tag actually created.
* New Orbital Tag effects no longer visually overlap their hand-level messages.

Improved XMult gain feedback.

* Consumption now shows the exact amount gained instead of the new total XMult.
* Charm Collector and Favorite Performance now show their XMult gain amount in Attention colour.

### JokerDisplay

Added JokerDisplay support for all 31 new Jokers.

* Added displays for Double Act and all 5 transformation Jokers.
* Added equality-condition displays for Juliette Mime, Livia Mime, Mireille Mime, and Double Act.
* Added random Tag chance displays for all new Tag Mimes.
* Added poker-hand and Orbital Tag displays for the new hand-progression Mimes.
* Added dynamic deck-scaling displays for Altered Deck, Marked Deck, Printed Deck, Patron's Aura, and Consumption.
* Updated Vivienne Mime to show the correct 1 in 4 chance.
* Livia Mime and Juliette Mime now display Hands = Discards without a money-digit check.

### Visuals and Feedback

Improved transformation presentation.

* Double Act, Casting Call, Outtake, Cue Card, Receipt, and Stage Prop now use a full flip-transform-reveal sequence.
* Added protection against duplicate transformation queues while an animation is already in progress.

Improved Tag presentation.

* New random Tag creators now follow Woman Mime-style event timing and sound feedback.
* Multi-Tag creation is presented one Tag at a time.
* Orbital Tag creation is queued after related hand-level feedback.

Improved cumulative XMult presentation.

* XMult growth popups now show the amount gained rather than an ambiguous total where appropriate.
* Gain values use Attention colour for clearer distinction from scoring payouts.

### Localization

Fully updated all 15 supported localization files for 1.13.0 content.

* English
* Russian
* German
* French
* Italian
* Spanish
* Latin American Spanish
* Brazilian Portuguese
* Polish
* Dutch
* Indonesian
* Japanese
* Korean
* Simplified Chinese
* Traditional Chinese

Added localization for:

* All 31 new Jokers.
* New Shift Reroll economy settings and preview behavior.
* New transformation, Tag, Orbital Tag, playing-card creation, and Double Act status messages.
* Updated Acid Deck and Acid Sleeve behavior.

Improved existing localization.

* Added the inactive `(Before Gold Cards)` timing note to Double Act.
* Updated Livia Mime and Juliette Mime descriptions to match their Hands = Discards condition.
* Corrected Russian wording and typo fixes, including Baron Mime's Mult text.
* Preserved the finalized English and Russian wording except where a real gameplay or display fix required a change.

### Assets

Expanded and validated 1x / 2x asset support for the new content.

* Added artwork for all new 1.13 Jokers.
* Added Mime Aura assets.
* Updated Joker, Deck, and Sleeve atlases where required by the new content.
* Preserved paired 1x / 2x dimensions and valid atlas coordinates.

### Fixes / Polish

* Fixed Blueprint copying for Monochrome Mime's Tag-trigger effect.
* Fixed Double Act family transformation timing and visual sequencing.
* Fixed duplicate or misleading popups for new Tag creators.
* Fixed Katarina Mime multi-Tag feedback.
* Fixed new Orbital Tag effects visually overlapping hand-level feedback.
* Fixed incremental XMult gain popups for cumulative XMult Jokers.
* Fixed Vivienne Mime's chance mismatch.
* Fixed Livia Mime and Juliette Mime equality logic and displays.
* Improved safe handling of delayed events and copying sources.
* Improved shop-row fallbacks and preview safety for Shift Rerolls.

### Notes

* This update adds 31 new Jokers.
* No existing Joker, deck, sleeve, Consumable, Tag, or mode was removed.
* The update focuses on Double Act transformations, Tag generation, poker-hand progression, deck-based XMult scaling, Shift Reroll expansion, Blueprint correctness, and release polish.
* Hidden Space Joker synergies remain intentionally discoverable through play.


## 1.12.1 - 2026-06-28 - Hotfix of Planetarium Update

### Fixes

* Fixed Aria Mime's sprite position.

  * Aria Mime was incorrectly assigned to the same atlas position as another 1.12.0 Mime.
  * Aria Mime now uses the correct atlas coordinates.
  * This fixes Aria Mime displaying the wrong sprite in-game, in the collection, and in card previews.

### Notes

* This is a small hotfix for the 1.12.0 Mime expansion.
* No gameplay values were changed.
* No new Jokers, decks, sleeves, consumables, or mechanics were added in this patch.


## 1.12.0 - 2026-06-28 - Planetarium Update

### New Jokers

Added 10 new Mimes focused on poker-hand leveling and reroll-based progression.

#### Space Joker Admirers

Added 9 fixed-hand Mimes.

* Added Aria Mime.

  * After each shop reroll, has a chance to level up High Card.
  * Has a hidden Space Joker synergy.
* Added Bianca Mime.

  * After each shop reroll, has a chance to level up Pair.
  * Has a hidden Space Joker synergy.
* Added Celeste Mime.

  * After each shop reroll, has a chance to level up Two Pair.
  * Has a hidden Space Joker synergy.
* Added Dahlia Mime.

  * After each shop reroll, has a chance to level up Three of a Kind.
  * Has a hidden Space Joker synergy.
* Added Elise Mime.

  * After each shop reroll, has a chance to level up Straight.
  * Has a hidden Space Joker synergy.
* Added Fiona Mime.

  * After each shop reroll, has a chance to level up Flush.
  * Has a hidden Space Joker synergy.
* Added Giselle Mime.

  * After each shop reroll, has a chance to level up Full House.
  * Has a hidden Space Joker synergy.
* Added Helena Mime.

  * After each shop reroll, has a chance to level up Four of a Kind.
  * Has a hidden Space Joker synergy.
* Added Isolde Mime.

  * After each shop reroll, has a chance to level up Straight Flush.
  * Has a hidden Space Joker synergy.

When Space Joker is present, these Mimes may create an Orbital Tag for their assigned poker hand.

#### Random Hand Level Mime

Added Amelia Mime.

* After each shop reroll, levels up a random visible poker hand.
* Blueprint compatible.
* Does not use the hidden Space Joker Orbital Tag synergy.

### New Decks

Added Coral Deck.

* After each defeated Boss Blind, invokes Coral Bloom.
* Coral Bloom creates a random Tag.
* Boss Tag is excluded from the random Tag pool.

Added Acid Deck.

* Starts with 2 Judgement cards.
* After each played hand or discard, invokes Oxidation.
* Oxidation attempts to destroy a random valid Joker, playing card, or Consumable.
* Eternal Jokers resist Oxidation.
* Negative cards are not protected from Oxidation.

### CardSleeves Compatibility

Added CardSleeves support for Pantomime Paradox decks.

* Added Chevron Sleeve.
* Added Pale Sleeve.
* Added Unbearable Sleeve.
* Added Coral Sleeve.
* Added Acid Sleeve.

Added special deck + sleeve combo behavior.

* Chevron Deck + Chevron Sleeve starts with Ancient Enlightenment instead of duplicating the normal Chevron setup.
* Pale Deck + Pale Sleeve starts with Vouch Coup.
* Unbearable Deck + Unbearable Sleeve starts with Negative Wraith and Negative Judgement.
* Unbearable Deck + Unbearable Sleeve can secretly increase the required winning Ante on shop reroll.
* Coral Deck + Coral Sleeve invokes Coral Bloom after defeated Small or Big Blinds instead of only Boss Blinds.
* Acid Deck + Acid Sleeve creates a Negative Judgement after each defeated Boss Blind.

### New Effects

Added Oxidation.

* Used by Acid Deck and Acid Sleeve.
* Can target Jokers, playing cards, and Consumables.
* Eternal Jokers resist the effect.
* The effect now waits until after hand scoring before resolving, so it no longer visually interrupts scoring effects such as Press.

Added Coral Bloom.

* Used by Coral Deck and Coral Sleeve.
* Creates a random Tag.
* Boss Tag is excluded.

### Joker Changes

Updated Queen Mime.

* Queen Mime now checks for Face cards instead of only Queens.
* Pareidolia synergy is supported.
* A numeric Straight with Pareidolia can trigger Queen Mime.
* Debuffed cards and Stone Cards still break the condition.

Updated Nebula Mime.

* Rarity changed from Common to Uncommon.
* Astral Queen synergy list now includes the new Space Joker Admirer Mimes.

Updated Wizard Mime.

* Rarity changed from Common to Uncommon.

Updated Stella Mime, Luna Mime, Comet Countess, Falling Asteroid, Final Lesson Lady, Monochrome Mime, and the new hand-level Mimes.

* Level-up messages now show the specific poker hand that was leveled up.
* Blueprint-compatible cards now attach the message to the Blueprint copy when appropriate.
* Hand-level effects now share safer helper logic.

### Tag Fixes

Fixed duplicate tag-trigger handling.

* Removed redundant manual tag-trigger dispatch from custom Tags.
* Abyssal Tag no longer causes duplicate tag-trigger reactions.
* Masked Mega Buffoon Pack Tag no longer causes duplicate tag-trigger reactions.
* Charm Collector now ignores duplicate trigger reports from the same Tag.
* Monochrome Mime now ignores duplicate trigger reports from the same Tag.

### JokerDisplay

Added JokerDisplay support for the new hand-level Mimes.

* Added display entries for all 9 fixed-hand Mimes.
* Added display entry for Amelia Mime.
* Added compact chance display for fixed-hand Mimes.
* Added poker-hand reminder text for each fixed-hand Mime.
* Hidden Space Joker Orbital Tag synergy is intentionally not shown in JokerDisplay.

Improved existing JokerDisplay definitions.

* Fixed Tenth Mime display counting.
* Tenth Mime now correctly counts valid held non-Face cards.
* Ace is now handled correctly in number-or-Ace helper logic.
* Fixed Tenth Mime fallback percentage.
* Fixed Jack Mime fallback percentage.
* Updated Queen Mime display to match its Pareidolia-compatible Face-card logic.
* Corrected several fallback values used by display previews.

### Localization

Fully updated supported localization files for 1.12.0 content.

* English
* Russian
* German
* French
* Italian
* Spanish
* Latin American Spanish
* Brazilian Portuguese
* Polish
* Dutch
* Indonesian
* Japanese
* Korean
* Simplified Chinese
* Traditional Chinese

Added localization for:

* New decks.
* New Jokers.
* CardSleeves descriptions.
* Oxidation.
* Coral Bloom.
* Acid Deck and Coral Deck messages.
* Space Joker Orbital Tag messages.
* Unbearable Deck + Unbearable Sleeve secret messages.
* Updated Queen Mime Face-card text.

### Fixes / Polish

* Fixed Acid Deck and Acid Sleeve timing so Oxidation resolves after hand scoring.
* Fixed poker-hand level-up messages that previously displayed only a generic Level Up message.
* Fixed CardSleeves localization structure.
* Fixed localization syntax issues across non-English localization files.
* Fixed missing localization keys for new 1.12.0 content.
* Fixed Russian localization wording and structure for 1.12.0.
* Fixed CardSleeves fallback behavior for missing or alternate sleeve text.
* Improved safety around hidden effects, delayed messages, and duplicate trigger contexts.

### Notes

* This update focuses on poker-hand progression, Planetarium-style synergies, CardSleeves support, new deck mechanics, localization completion, and stability polish.
* The hidden Space Joker synergy is intentionally discoverable through play rather than fully exposed in descriptions.


## 1.11.1 - 2026-06-21 - Stability Hotfix

### Compatibility Fixes

* Updated Unbearable Deck behavior in Multiplayer / Experimental Multiplayer runs.

  * In single-player runs, skipping a Blind still increases the required score as before.
  * In Multiplayer / Experimental Multiplayer runs, skipping a Blind no longer increases the required score.
  * Instead, Unbearable Deck now removes money equal to the current `current_money_delta` value.
  * This Multiplayer skip penalty does not change `current_money_bonus`.
  * This Multiplayer skip penalty does not advance or modify the boss money-penalty ladder.

### Firstlastro Fixes

* Improved Firstlastro swap timing.

  * Overflow checks now resolve one card at a time.
  * Each Joker / Consumable overflow check now waits at least 0.5 seconds before the next check.
  * This makes Eternal, Negative, and Removed results easier to read during the swap sequence.
* Updated the Firstlastro swap start message.

  * The main swap message is now displayed on the screen instead of being attached to the first Joker.
  * The message now uses the same general screen-style presentation as Unbearable Deck messages.
* Preserved Firstlastro trigger rules.

  * Firstlastro still triggers only from the first vanilla shop reroll in each shop.
  * Shift Rerolls still do not trigger Firstlastro.
  * Free vanilla rerolls can still trigger Firstlastro.

### Asteroid Joker Balance / Clarity

* Updated Falling Asteroid and Prismatic Asteroid upgrade counting.

  * Asteroids now count Enhancements, Seals, and Editions as separate upgrade components.
  * Each component contributes +1 to the upgrade count.
  * Example: a Bonus Card with a Blue Seal now counts as 2 upgrade components.
  * Example: an unmodified card, a Gold Card, and a Bonus Card with a Blue Seal count as 3 total upgrade components.
* Updated JokerDisplay support for the new Asteroid counting logic.

  * Display values now match the real in-game calculation.
  * The display no longer uses the older enhancement-only count.

### Config UI Polish

* Updated Sacrificetro and Firstlastro config-tab token behavior.

  * Restored the stable interactive boss-token style behavior for the mode icons.
  * Preserved sharper pixel-art icon rendering.
  * Preserved tooltip / hover support for the mode icons.
* Kept the dedicated config tabs for Sacrificetro and Firstlastro.

### Notes

* This is a stability and behavior-correction patch for the 1.11.0 Biblical Modes Update.
* No new Jokers were added in this patch.
* No new modes were added in this patch.


## 1.11.0 - 2026-06-16 - Biblical Modes Update

### New Optional Mode: Sacrificetro

Integrated the former standalone Sacrificelatro concept into Pantomime Paradox as a new optional config-only mode.

* Added Sacrificetro as a disabled-by-default run modifier.
* Sacrificetro is controlled only from the mod config tab.
* No New Run toggle is added for this mode.
* When enabled, Jokers and playing cards receive a Sacrifice sticker.
* At the end of each won round, eligible Sacrifice-stickered cards may be destroyed.
* Default destruction chance is 1 in 3.
* Added config options for:
  * Enabling Sacrificetro.
  * Affecting Jokers.
  * Affecting playing cards.
  * Adjusting the Sacrifice destruction odds.
* Eternal Jokers are protected from Sacrificetro destruction and show an Eternal message instead.
* Added legacy compatibility for the old `sac_sacrifice` sticker key.
* Added conflict protection against the old standalone Sacrificelatro / Sacrificetro mod IDs.

### New Optional Mode: Firstlastro

Added Firstlastro, a new optional mode inspired by Matthew 20:16.

* Added Firstlastro as a disabled-by-default run modifier.
* Firstlastro is controlled only from the mod config tab.
* No New Run toggle is added for this mode.
* The first vanilla shop reroll in each shop swaps the current Joker slot limit with the current Consumable slot limit.
* Shift Rerolls do not trigger Firstlastro.
* The mode triggers once per shop / blind.
* Reroll price does not matter: paid and free vanilla rerolls can both trigger the mode.
* After the slot swap, overflow cards are removed from left to right.
* Overflow removal checks the real current card count after every successful removal.
* Jokers are processed before Consumables.
* Eternal cards resist overflow removal and show an Eternal message.
* Negative cards resist overflow removal, show a Negative message, and use the Negative sound.
* Removed overflow cards show a Removed message and use a glass-breaking style destruction effect.

### Config UI

Added dedicated config tabs for the new modes.

* Added a Sacrificetro config tab.
* Added a Firstlastro config tab.
* Added large interactive boss-token style icons for both tabs.
* Added Biblical flavor text and tooltip lines for both modes.
* Fixed mode icon rendering to use sharper nearest-neighbor filtering.
* Rebuilt mode icons in strict 1x / 2x pixel-art sizes.

### Multiplayer / Compatibility

Improved safety around optional run modifiers.

* Sacrificetro settings can be synchronized through Multiplayer lobby config when available.
* Firstlastro remains tied to local vanilla shop reroll behavior.
* Shift Rerolls remain independent from Firstlastro triggers.
* Added safer config-only behavior so the new modes do not silently activate from the New Run screen.
* Added run-state snapshot behavior where needed so mode activation remains stable during a run.

### Localization

Added English and Russian localization for the new modes.

### Assets

Added new pixel-art assets.

* Added Sacrificetro boss-token icon.
* Added Firstlastro boss-token icon.
* Added Sacrifice sticker asset.
* Added 1x and 2x versions for all new mode assets.


## 1.10.0 - 2026-06-07 - Shift Rerolls Update

### New Feature: Shift Rerolls

Added **Shift Rerolls**, an optional local shop tool focused on controlled deck-building.

* Shift Rerolls can be enabled from the mod config.
* When enabled, a draggable **Shift Rerolls** panel appears in the shop.
* The panel allows shifting the current shop row forward or backward through a seeded list of registered shop items.
* Shift Rerolls can transform shop cards between supported Jokers and Consumables.
* The first Shift Reroll in a run costs **$0**.
* Each next Shift Reroll in the same run costs **+$1**.
* Shift Reroll cost is tracked per run.
* Shift Rerolls are local-only and are not synchronized in Multiplayer.

### Shift Reroll List

Added a dedicated Shift Reroll list overlay.

* The list shows all currently registered supported shop items.
* The list order can be seeded per run.
* The same run seed gives the same Shift Reroll order.
* Added filters for:

  * All items
  * Jokers
  * Consumables
  * Tarot cards
  * Planet cards
  * Spectral cards
* Added shop focus navigation for quickly jumping to the current shop cards inside the list.
* Added support for configurable list density:

  * 5 to 18 items per page.
  * Default: 8 items per page.
* Added an optional technical key column.

  * Default: hidden.
  * When disabled, item names get more space in the list.
* Added compact scaling for dense list pages.

### Shift Rerolls Config

Added a new **Shift Rerolls** config tab.

* Added toggle for enabling Shift Rerolls.
* Added toggle for seeding the list by run seed.
* Added toggle for triggering shop reroll effects.
* Added toggle for wrapping the list.
* Added configurable item count per list page.
* Added toggle for showing item keys.
* Added Reset Panel Position button.
* Removed the config-side Open Shift List button to avoid menu overlay issues.

### UI / UX

Improved Shift Rerolls panel behavior.

* The shop panel can now be dragged by its title area.
* The panel position is remembered for the current run.
* The default panel position now appears near the shop row instead of the upper-left area.
* The panel remains usable after leaving and re-entering the shop.
* Improved button behavior for `-1`, `List`, and `+1`.
* Improved list layout readability with and without item keys.
* Improved current-shop markers inside the list.

### Multiplayer Compatibility

Added basic compatibility support for **Multiplayer Experimental 0.7**.

* Added a dedicated Experimental Multiplayer compatibility layer.
* Experimental MP is detected even when its runtime finishes loading after Pantomime Paradox.
* Host-selected Pantomime Paradox run modifiers are treated as authoritative in Experimental Multiplayer lobbies.
* Task Mode, Hard Mode, and Impossible Mode settings can be synchronized from host to guest.
* In Multiplayer, Task Mode is forced to the Every Ante variant.
* In Multiplayer, Task Mode failures continue to use the money penalty behavior instead of run defeat.
* Existing standard Multiplayer compatibility remains preserved.
* The old CO-OP addon was not changed.

### Localization

Fully updated supported localization files for 1.10.0 content.

* English
* Russian
* German
* French
* Italian
* Spanish
* Latin American Spanish
* Brazilian Portuguese
* Polish
* Dutch
* Indonesian
* Japanese
* Korean
* Simplified Chinese
* Traditional Chinese

### Fixes / Polish

* Fixed Shift Rerolls shop panel interaction.
* Fixed Shift Rerolls panel position persistence during a run.
* Fixed Shift Reroll list navigation around current shop cards.
* Fixed Shift Reroll list readability for dense pages.
* Fixed localization structure issues in affected localization files.
* Preserved Chevron Deck shop behavior when Shift Rerolls are used.
* Cleaned up Shift Rerolls config layout.
* Cleaned up Shift Rerolls dictionary strings.


## 1.9.1 - 2026-05-31 - Visual Polish and Balance Hotfix

### Balance Changes

* Updated Abyssal Tag odds.

  * Negative Soul chance reduced from 30% to 15%.
  * Negative Hydro chance increased from 70% to 85%.

### Joker Changes

* Updated Mime Alchemist.

  * When the most played poker hand is discarded, Mime Alchemist now gives Magical edition to up to 3 random held cards without an edition.
  * If there are no valid held-card targets, the secret Creatrix effect triggers instead.
  * Creatrix adds a random Tag.
  * Boss Tag is excluded from the random Tag pool.
* Updated Wizard Mime.

  * Wizard Mime now adds a random Tag when its effect triggers.
  * The Tag is added even if there is no room to create the Potion card.
  * Potion creation still requires room.
  * Boss Tag is excluded from the random Tag pool.

### Fixes

* Fixed misleading scoring visuals for Stella Mime.

  * Stella Mime now levels up a random poker hand after the played hand is scored.
  * This prevents confusing intermediate Chips / Mult preview values during scoring.
* Improved level-up effect messaging.

  * Stella Mime now reports the specific poker hand that was leveled up.
  * The effect no longer appears as a misleading scoring-row bonus.
* Fixed Wizard Mime behavior when consumable slots are full.

  * The random Tag is no longer blocked by lack of room for Potion.

### JokerDisplay

* Updated Mime Alchemist display.

  * Display now shows whether the next trigger will give Magical editions or fall back to a Tag.
  * Magical preview now supports x1, x2, and x3 target counts.
* Updated Wizard Mime display.

  * Display now reflects the Potion + Tag effect more clearly.
  * The Tag portion is not tied to consumable slot availability.
* Updated Stella Mime display and messaging to better match its post-scoring level-up timing.

### Art / Visual Polish

* Replaced several Joker sprites with cleaner, more readable pixel-art versions.

  * Chrome Plate
  * Adamant Core
  * High Rank Sign
  * Broken Double Six
  * Falling Asteroid
  * Prismatic Asteroid
* Improved small-size readability for the updated sprites.
* Reduced noisy texture detail in favor of flatter, clearer Art Deco-style shapes.

### Localization

* Updated affected localization text for Stella Mime.
* Updated affected localization text for Mime Alchemist.
* Updated affected localization text for Wizard Mime.
* Updated Abyssal Tag odds text to match the new 85% / 15% split.
* Added / updated Creatrix messaging for Mime Alchemist's secret fallback effect.
* Cleaned up wording so the descriptions better match real trigger timing and slot requirements.

### Notes

* This patch focuses on post-1.9.0 cleanup, visual clarity, and behavior polish.
* No new Jokers were added in this patch.
* The main gameplay changes are the Mime Alchemist rework, Wizard Mime Tag behavior, Stella Mime scoring-visual fix, and Abyssal Tag odds adjustment.

## 1.9.0 - 2026-05-26 - Astral Update

### New Jokers

Added 5 new Jokers focused on poker hand leveling, Tags, rerolls, and cosmic scaling.

#### Poker Hand Level Jokers

  * Added Stella Mime

    * After each played hand, levels up a random visible poker hand.
    * Blueprint compatible.
  * Added Luna Mime

    * After each discard, levels up a random visible poker hand.
    * Blueprint compatible.
  * Added Comet Countess

    * Has a chance to level up a random visible poker hand for each discarded card.
    * Also checks sold Jokers and sold Consumables.
    * Blueprint compatible.
  * Added Orbit Duchess

    * Before each played hand is scored, has a chance to create a random Tag.
    * The chance is based on the current remaining Hands and Discards.
    * Blueprint compatible.

#### Reroll Joker

  * Added Invisible Mime

    * Has a chance to gain Charge on shop reroll.
    * When sold with enough Charges, duplicates the leftmost non-Invisible Mime Joker.
    * Higher Charge counts can grant hidden bonus rewards.
    * Not Blueprint compatible.

### New Tag

  * Added Abyssal Tag

    * Creates a Negative Hydro or Negative Soul card.
    * Uses a 70% / 30% split between Hydro and Soul.
    * Appears as a rare Tag starting from Ante 2.
    * Added Abyssal Tag to supported random Tag pools.

### Reworks / Changes

  * Reworked Nebula Mime.

    * Nebula Mime now gains its bonus from both played poker hands and discarded poker hands.
    * Played hand scaling now happens before the hand's own scoring payout.
    * Its scaling is now based on the poker hand level multiplied by Astral Queen.
    * Astral Queen counts:
      * Planet cards in Consumable slots.
      * Listed cosmic Jokers.
      * Listed bought Vouchers.
    * Added the new cosmic Jokers to Nebula Mime's Astral Queen synergy list.
    * Blueprint copies only the current payout and does not increase Nebula Mime's stored bonus.
  * Updated Mimetracte.

    * Its final-hand held-card bonus now gives +45% of current Chips instead of a flat +45 Chips.
  * Updated Tag Repertoire.

    * It now creates 1 to 3 random Tags at end of round.
    * Boss Tag remains excluded.
    * Added sound feedback when Tags are created.
  * Updated Monochrome Mime.

    * Rarity changed from Common to Uncommon.

### JokerDisplay

  * Added JokerDisplay support for all new 1.9.0 Jokers:
    * Stella Mime
    * Luna Mime
    * Comet Countess
    * Orbit Duchess
    * Invisible Mime
  * Updated new Joker displays to use compact vanilla-style formatting.
  * Chance displays now use concise green formatting such as `(1 in 6)`.
  * Invisible Mime display now shows its current Charge progress and reroll chance.

### Localization

  * Updated English and Russian localization for all new 1.9.0 content.
  * Updated existing supported localizations for 1.9.0 content:
    * German
    * Spanish
    * Latin American Spanish
    * French
    * Italian
    * Brazilian Portuguese
  * Added / completed additional supported localization files:
    * Dutch
    * Polish
    * Indonesian
    * Japanese
    * Korean
    * Simplified Chinese
    * Traditional Chinese

### Fixes / Polish

  * Fixed Masked Mega Buffoon Pack Tag queue behavior.

    * It now resolves in the correct Tag queue order.
    * It no longer waits incorrectly until Blind selection when created from other sources.
    * It no longer risks blocking the game with a stuck event.
  * Fixed Abyssal Tag queue behavior.

    * It now resolves correctly with other queued Tags.
    * It no longer blocks subsequent Tag effects.
  * Improved random Tag behavior for Sigma Mime and related Tag sources.
  * Cleaned up affected tooltip descriptions and supporting dictionary strings.

## 1.8.2 - 2026-05-23 - Localization and Stability Patch

### Localization

  * Added German localization.
  * Added French localization.
  * Added Spanish localization for Spain.
  * Added Spanish localization for Latin America.
  * Added Brazilian Portuguese localization.
  * Added Italian localization.
  * Synchronized the new localization files with the current English text structure.
  * Preserved all Balatro/SMODS formatting tags, variables, tooltip references, and placeholders across the new localization files.

### Fixes

  * Fixed Favorite Performance behavior.
    * It now gives its current XMult bonus on any played hand.
    * Its bonus now increases only when the played hand is the most played poker hand this run.
    * Blueprint effects still copy only the current XMult bonus without increasing it.

  * Fixed Masked Mega Buffoon Pack Tag context handling.
    * The Tag now correctly reports a successful Tag trigger.
    * Charm Collector now correctly detects this custom Tag when it is used.

  * Fixed Chevron Deck shop behavior after buying Overstock or Overstock Plus.
    * Newly added shop slots now correctly generate shop card UI.
    * Cards created in the new slot now correctly show price and Buy / Buy and Use buttons.

  * Fixed Monochrome Mime trigger coverage.
    * It now also works when a Booster Pack is skipped.
    * Existing triggers for Booster Pack opening, Voucher purchase, and Tag use are preserved.

### Balance Changes

  * Mime-Polis is now a Common Joker.

### Notes

  * This patch focuses on localization coverage, shop UI stability, and several post-1.8.0 behavior fixes.
  * No new Jokers were added in this patch.

## 1.8.1 - 2026-05-18 - Balance and Fix patch

### Balance Changes
- **Baron Mime** rarity changed from Rare to Uncommon.
- **Second Mime** rarity changed from Uncommon to Common.
- **Eighth Mime** rarity changed from Uncommon to Common.
- **Nebula Mime** rarity changed from Rare to Common.
- **Polished Payroll** rarity changed from Uncommon to Common.

### Reworks / Changes
- Reworked **Curator Violet**.
  - Curator Violet now follows an Idol-style selected card.
  - Each held copy of the selected card gives XMult when scored.
  - The XMult bonus scales from the number of selected-card copies in the full deck.
  - **Showman** now increases Curator Violet's per-copy scaling bonus.
  - Updated **Curator Violet** JokerDisplay support to show the real total XMult that will be applied.

- Improved **Opening Gesture Mime**.
  - It now gives Chips to every scoring card in the played hand.
  - The first card held in hand still keeps its Chips bonus.
  - Updated JokerDisplay support to better reflect the expanded effect.

- Improved **Mime Illusionist**.
  - If the second-to-last Joker is Common, it can still transform into an Uncommon Joker.
  - If the second-to-last Joker is Uncommon, it can still transform into a Rare Joker.
  - If the second-to-last Joker is already Rare, it now transforms into another random Rare Joker.
  - Duplicate Mime Illusionist effects remain non-multiplicative.

- Improved **Sapphire Mime**.
  - It can now create either **Immolate** or **Hydro** at the start of round.
  - The selection is split between both Spectral cards.

- Improved **Glass Mime**.
  - The created Glass playing card now always receives either a random Seal or a random Edition.

### Boss Blind Behavior
- Updated **Eighth Mime** Boss Blind behavior.
  - Eighth Mime is no longer fully inactive on Boss Blinds.
  - On Boss Blinds, only the rank/suit transformation is disabled.
  - Edition, Seal, and Enhancement transformations can still trigger on Boss Blinds.

### JokerDisplay
- Updated **Curator Violet** display.
  - Main display now shows the total XMult that will be applied for the current held target cards.
  - Reminder text now shows the current Idol-style selected card.
- Updated **Opening Gesture Mime** display.
  - Display now reflects its scoring-card and first-held-card Chips bonus more clearly.

### Fixes / Polish
- Updated affected English and Russian localization text.
- Cleaned up several tooltip descriptions to better match the new 1.8.1 behavior.
- Preserved Blueprint compatibility behavior for the adjusted creation and scoring effects.

## 1.8.0 - 2026-05-09 - Major Update

### New Jokers

Added a new wave of Jokers focused on poker hand history, Booster Pack interactions, Tags, Enhanced Cards, and rank-based builds.

#### Poker Hand Jokers

- Added **Last Curtain Lady**
  - On your last discard of round, earns money equal to the number of times the discarded poker hand was played this run.

- Added **Opening Gesture Mime**
  - The first card held in hand and the first scoring card each give Chips equivalent to the number of times the played poker hand was played this run.

- Added **Final Lesson Lady**
  - At end of round, levels up a random visible poker hand.

- Added **Favorite Performance**
  - If played hand is your most played poker hand, gains XMult per level of that hand.
  - Blueprint copies only the current XMult bonus.

- Added **Collection Mime**
  - When any poker hand is played, gains Chips equivalent to the number of times that hand was played this run.
  - Blueprint copies only the current Chips bonus.

#### Pack, Tag, and Voucher Jokers

- Added **Courier Mime**
  - On your last discard of round, creates a random Tarot, Planet, or Spectral card.
  - Must have room.

- Added **Monochrome Mime**
  - When a Booster Pack is opened, a Voucher is bought, or a Tag is used, levels up a random visible poker hand.

- Added **Broken Double Six**
  - After skipping 6 Booster Packs, turns into Oops! All 6s.

- Added **Charm Collector**
  - When any Tag is used, gains XMult.
  - Blueprint copies only the current XMult bonus.

#### Economy and Condition Jokers

- Added **Bronze Scratch Ticket**
  - Each discarded card has a chance to give money.

- Added **High Rank Sign**
  - If played poker hand level is higher than current Ante, destroys a random card held in hand after scoring and gives money.

- Added **Polished Payroll**
  - If all scoring cards in played poker hand are Enhanced Cards, gives money.

#### Enhanced Card Jokers

- Added **Chrome Plate**
  - Enhanced cards held in hand or played and scored give Chips.

- Added **Adamant Core**
  - Enhanced cards held in hand or played and scored give Mult.

- Added **Prismatic Asteroid**
  - If played hand contains cards with enough different Enhanced types, levels up the played poker hand.
  - Checks the full played hand, including non-scoring cards.

- Added **Falling Asteroid**
  - If discard contains cards with enough different Enhanced types, levels up the discarded poker hand.

#### Rank Retrigger Jokers

Added a new rank-based retrigger cycle. These Jokers retrigger all played and held cards of a specific rank one more time.

- Added **Deuce Signal**
- Added **Trey Signal**
- Added **Four Signal**
- Added **Five Signal**
- Added **Six Signal**
- Added **Seven Signal**
- Added **Eight Signal**
- Added **Nine Signal**
- Added **Ten Signal**
- Added **Ace Signal**

Added three face-card rank retrigger Mimes:

- Added **Jack of Mimes**
- Added **Queen of Mimes**
- Added **King of Mimes**

### JokerDisplay

Added JokerDisplay support for all new 1.8.0 Jokers.

Improved JokerDisplay styling across many existing Jokers:

- Updated chance text formatting to better match vanilla JokerDisplay style.
- Reduced overly long display strings.
- Improved reminder text formatting.
- Fixed several spacing issues.
- Fixed color styling for selected symbols and keywords.
- Updated rank retrigger Joker displays to match the existing Mime of Diamonds style.

Specific JokerDisplay fixes:

- **Curator Violet**
  - Main display now shows the total current bonus.
  - Multiplier breakdown was moved to the extra line.

- **Lab Assistant Mime**
  - Fixed slash formatting in Shard/Crystals display.

- **Sixth Mime**
  - Main display now uses a cleaner “Creates card” style.

- **Ruby Mime**, **Lapis Mime**, **Amber Mime**, **Amethyst Mime**
  - Removed extra spacing in main display strings.

- **Nebula Mime**
  - Fixed color styling on the final display line.

- **Eighth Mime**
  - Removed unnecessary spaces around slash-separated options.

- **Mime Agony**
  - Fixed color styling for + and % symbols.

- **Return Package**
  - Fixed money preview calculation for the current discard.

- **Chrome Plate** and **Adamant Core**
  - Main display now shows the calculated total bonus instead of a formula-style line.
  - Enhanced reminder text now uses the correct attention color.

### Fixes

- Fixed Blueprint behavior for **Favorite Performance** and **Collection Mime**.
  - Blueprint now copies the stored bonus correctly without increasing it.

- Fixed Blueprint animation and message behavior for **Prismatic Asteroid**, **Falling Asteroid**, and **Monochrome Mime**.
  - These now follow the same visual pattern as Final Lesson Lady.

- Fixed Enhanced type detection for Asteroid Jokers.
  - Stone Cards are now correctly recognized.
  - Debuffed cards are ignored as ballast for Asteroid conditions.

- Fixed **Polished Payroll** condition.
  - It now checks only the scoring poker hand, not every played card.
  - Debuffed scoring cards fail the condition.

- Fixed **Monochrome Mime** trigger coverage.
  - It now works on Booster Pack opening, Voucher purchase, and Tag use.

- Fixed **High Rank Sign** timing.
  - It now destroys the held card after scoring, preventing held-card scoring conflicts.

- Fixed Wild Card handling for the previous Monochrome Mime design during development.

## 1.7.1 - 2026-04-22 - Multiplayer compatibility hotfix

### Fixes
- Fixed Multiplayer compatibility for Task Mode.
- Fixed Multiplayer compatibility for Hard Mode.
- Fixed Multiplayer compatibility for Impossible Mode.
- Fixed lobby synchronization for TDPP multiplayer modifiers.
- Fixed mode synchronization when creating, updating, and starting Multiplayer lobbies.
- Improved compatibility when using Pantomime Paradox together with the Multiplayer mod.

### Notes
- Multiplayer support for Task/Hard/Impossible modes now works correctly for host and guest.
- Sigma Mime can no longer appear with Eternal or Perishable stickers.

## 1.7.0 - 2026-04-21 - Major Update

### Added
- Added 4 new Vouchers:
  - **Foil Package**
  - **Collection Album**
  - **Voucher Ledger**
  - **Tag Repertoire**
- Added several new hidden Joker synergies.
- Added Stone Cards as valid targets for **Wild Marble**.

### Changed
- Reworked **Wild Marble** so its effect now also counts held **Stone Cards**.
- Rebalanced **Lady Mime** with a new hidden synergy.
- Rebalanced **Verda Mime** with a new hidden synergy.
- Rebalanced **Curator Violet** with a new hidden synergy.
- Rebalanced **Mime Agony** with a new hidden synergy.
- Updated multiple Joker descriptions and supporting localization text for 1.7.0 changes.
- Standardized many **JokerDisplay** entries to better match vanilla-style formatting and reminders.

### Fixed
- Fixed multiple **JokerDisplay** formatting inconsistencies.
- Fixed missing inactive-style reminder brackets on various Joker displays.
- Fixed spacing issues in several Joker displays (for example, values now display like `6x65%` instead of `6 x 65%`).
- Fixed **Wild Marble** display/support text so it correctly reflects Stone Card support.
- Fixed dynamic value presentation for several updated Jokers so their displayed values stay in sync with their current behavior.

## 1.6.2 - 2026-04-14 - Important Fix patch

### Balance Changes
- **Miner Mime** now retriggers played and held in hand **Stone** cards **2 additional times** instead of 1.
- Simplified the **Queen's Order** challenge:
  - Added **+2 Joker slots**
  - Added a starting **Pareidolia**
- Simplified the **Tired Rulers** challenge:
  - Added **+2 Joker slots**
  - Added a starting **Pareidolia**

### Fixes
- Reworked **Faded Seal** random bonus shift logic so its minimum and maximum roll bounds now correctly account for the current global normal probability.
- Fixed **Faded Seal** tooltip values so the displayed random range now matches the real in-game behavior.
- Improved **Faded Seal** localization text for better clarity and accuracy.

## 1.6.1 - 2026-04-12 - Important Fix + Balance patch

### Balance / Reworks
- **Nebula Mime** has been reworked to grant **+% of current Chips** instead of flat Chips.
- **Nebula Mime** now scales its bonus from the level of the discarded poker hand.

### Gameplay
- **Eighth Mime** has been significantly expanded.
- Instead of only turning a random held card into a **Wild 8**, it now has a chance to randomly modify **one** of several parameter groups on a held card:
  - **rank and suit** → **8 of Spades**
  - **Edition**
  - **Seal**
  - **Enhancement**
- The original trigger condition remains unchanged.

### Art / Visual Fixes
- Adjusted and polished several joker artworks.

### Localization
- Updated **English** localization for the changed jokers and improved wording in several affected lines.
- Updated **Russian** localization for the changed jokers and synchronized the new descriptions with gameplay behavior.
- Clarified tooltip wording around debuffed-card interactions where needed.

### Compatibility / UI
- Updated **JokerDisplay** support for **Nebula Mime** and **Eighth Mime**.
- Added JokerDisplay key updates for **Wild Marble** and **Prism of Edith**.

### Polish
- Improved consistency of tooltip phrasing for recently adjusted Mime jokers.
- Cleaned up release text for a more accurate and polished 1.6.1 patch.

## 1.6.0 - 2026-04-09 - Content Update

### Added
- Added 8 new Mime Jokers:
  - **Golden Judith** — Retriggers played and held Gold cards 1 additional time.
  - **Chrome Vera** — Retriggers played and held Steel cards 1 additional time.
  - **Crystal Iris** — Each held Glass card gives +25% of current Chips.
  - **Mosaic Flora** — Each held Bonus, Mult, or Wild card gives +25% of current Chips.
  - **Curator Violet** — Each Enhanced card in your full deck gives +1% of current Chips.
  - **Leading Lady** — The leftmost held card gives +25% of current Chips.
  - **Prism Edith** — Each held card with any Edition gives +25% of current Chips.
  - **Sigil Nora** — Each held card with any Seal gives +25% of current Chips.

- Added DisplayJoker support for all new Mime Jokers.

### Changed
- Simplified **Leading Lady**:
  - Removed hand-size scaling.
  - The effect now always grants a fixed +25% of current Chips to the leftmost held card.

### Notes
- This update expands the Mime roster with a new enhancement-focused set of Jokers built around Gold, Steel, Glass, Editions, Seals, and other enhanced card synergies.
- Multiplayer Task Mode note: Task Mode is currently not fully synchronized with the Multiplayer lobby/run state, so the automatic Multiplayer override to Every Ante may fail and a failed task may still behave like the Singleplayer version instead of using the intended Multiplayer money penalty. In practice, the current Multiplayer integration can fall back to the local Task Mode menu state instead of always reading a fully synchronized MP state, which is why behavior may differ between host and guest. As a temporary workaround, Task Mode can still be played in Multiplayer if the guest enables Task Mode in the Singleplayer menu before joining or starting the Multiplayer run; for the most consistent results, it is recommended that both players set it up beforehand and manually use the Every Ante variant when needed. This is a known compatibility limitation between Pantomime Paradox Task Mode and the current Multiplayer state-sync flow, and it does not affect normal Singleplayer Task Mode behavior.

## 1.5.7 - 2026-04-05 - Fix and Content Update

### Added
- Added **Florist Mime**
- Added **Nebula Mime**
- Added **JokerDisplay** support for **Florist Mime**
- Added **JokerDisplay** support for **Nebula Mime**

### Changed
- Reworked a large part of **JokerDisplay** support to reduce lag and microstutters
- Optimized display calculations by moving repeated hand / held-card / suit / enhancement checks into shared helpers
- Improved **JokerDisplay** stability when many Jokers are present at once
- Polished several display reminders and formatting details for better vanilla-style readability
- Updated **King Mime** display reminder formatting
- Improved handling of our custom **Magical** edition in Joker-related display text where applicable

### Fixed
- Fixed multiple **JokerDisplay** calculations that could return invalid values or `ERROR`
- Fixed heavy display calculations for several Mime Jokers that were repeatedly recalculating the same hand state
- Fixed missing reminder arrow on **King Mime**
- Fixed **JokerDisplay** crashes caused by the experimental global **Magical** edition display integration
- Fixed several custom display lines to better match the actual live effect of their Jokers

### Notes
- The new **JokerDisplay** optimization pass focused on performance and stability first
- The experimental global automatic display line for the custom **Magical** edition was rolled back for stability

## 1.5.6.1 - 2026-04-05 - Hotfix

### Fixed
- Restored the correct localization text for **Ninth Mime**
- Restored the correct localization text for **Wizard Mime**

### Compatibility
- Tightened optional mod detection for **JokerDisplay**
- Tightened optional mod detection for **Multiplayer**
- Optional compatibility branches now initialize only when their target mod is actually active

### Notes
- This patch does **not** resolve lag caused by **Multiplayer** remaining inside the `Mods` folder
- If you are not actively testing Multiplayer compatibility, it is recommended to keep the mod outside the `Mods` folder

## 1.5.6 - 2026-04-05 - Fix + Сompatibility patch

### Added
- Completed **JokerDisplay** support for the remaining **Pantomime Paradox** Jokers.
- Added a new **Config** toggle to enable or disable **Pantomime Paradox Joker Displays** when **JokerDisplay** is installed.
- Added conditional detection so the Joker Display toggle only appears if the **JokerDisplay** mod is present.

### Changed
- Standardized many Joker Display reminder lines to better match vanilla-style **JokerDisplay** formatting.
- Improved multiple display texts to be shorter, cleaner, and more readable during runs.
- Updated several reminder displays to use more consistent bracketed formatting and color usage.
- Refined odds display formatting to better match the expected vanilla-style presentation.
- Adjusted several display reminders and labels for clarity across the full Joker roster.

### Polish
- Improved coloring on multiple Joker Displays for better readability and consistency.
- Refined special reminder text formatting for several Jokers, including edition-based, spectral, and status-style reminders.
- Updated the **Fourth Dimension** display so **Wild 4** uses the proper spectral-style color treatment.
- Improved the **White Mime** display so **Negative** uses the correct negative-style color treatment.
- Cleaned up several displays by removing redundant reminder words such as extra “Again” text where unnecessary.

### Notes
- Changing the new **Joker Display** Config toggle currently requires a game restart to fully apply.
- No gameplay balance changes were made in this patch; this update focuses on **JokerDisplay completion, readability, and Config integration**.

## 1.5.5 - 2026-04-02 - Fix + Сompatibility patch

### Added
- Added a new **Jokers Buffs** config tab while keeping the original **Config** tab for main mod settings.
- Added the initial **compatibility framework** for external mod support.
- Added the first large wave of **JokerDisplay** support for TDPP jokers.
- Added the second wave (**2A**) of **JokerDisplay** support for additional medium-complexity jokers.
- Added the third wave (**2B**) of **JokerDisplay** support for more medium-complexity jokers.

### Changed
- Reorganized mod settings so core options remain in **Config**, while joker buff toggles are grouped under **Jokers Buffs**.
- Improved several **JokerDisplay** layouts to use more compact and readable reminder text.
- Adjusted **Blue Mime**, **Red Mime**, and **Gold Mime** displays to show the real total value they will grant for the currently evaluated hand instead of a static per-card value.
- Refined several order-dependent **JokerDisplay** entries to show clearer formulas/state info instead of misleading pseudo-exact totals.

### Fixed
- Fixed the config menu crash caused by returning the wrong structure from `config_tab`.
- Fixed empty red display blocks appearing on some `XMult` JokerDisplay entries.
- Fixed oversized or awkward multi-line display text for several jokers by shortening reminder strings.
- Fixed misleading display totals for some jokers whose effects depend on current hand state or scoring order.

### Compatibility
- Added groundwork for future **Multiplayer** compatibility auditing.
- Separated display-side compatibility logic from gameplay logic to reduce the risk of conflicts with other mods.

## 1.5.4 - 2026-04-02 - Fix patch

### Fixes

- Added improved compatibility with Balatro Multiplayer.
- Fixed TDPP multiplayer-specific mode behavior incorrectly affecting normal Single Run games.
- Fixed host-selected TDPP mode toggles not syncing correctly to the guest in real PvP runs.
- Adjusted Task Mode behavior in Multiplayer:
  - Multiplayer now uses the Every Ante variant during real PvP runs.
  - failing a task in Multiplayer no longer causes a TDPP-specific game over;
  - instead, the task panel turns red and applies a fixed **-$16** penalty.
- Adjusted Hard Mode and Impossible Mode for Multiplayer compatibility:
  - their Multiplayer behavior now applies only during real PvP runs;
  - normal Single Run behavior remains unchanged.
- Fixed Multiplayer run-state detection so Single Run and PvP are handled separately.

### Joker Fixes

- **Emerald Mime**
  - now avoids reapplying the card's current seal when choosing a new one;
  - multiple copies can now reroll seals more cleanly in sequence.
- **Garnet Mime**
  - now avoids reapplying the card's current edition when choosing a new one;
  - multiple copies can now reroll editions more cleanly in sequence.

### Notes

- Chevron Deck's rare edition-tag interaction was intentionally left unchanged.

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
