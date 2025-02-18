---
layout: page
title: System Changelog
permalink: /changelogs/system
---

## [1.3.063] - Darkmantle: Improved Chat Messages & V13 Support
Introduces new chat message types for combat turns, rests, and activations which include consumption/recovery details. Also adds initial support for Foundry V13.

### Improvements
- Added custom chat message type for combat turns, rests, and activations ([#583], [#933], [#936])
- Converted remaining config applications to `ApplicationV2` ([#931])
- Added combat message activation types ([#936])

### Compendium Content
- Change Bone Devil to be a devil ([#932])

### Bug Fixes
- Rest chat messages should now display properly if they have rolls ([#579])
- Fixed a variety of UI issues when running in V13 ([#904])
- Context menus should now open when running in V13 ([#928])
- Table of contents and item compendiums should now open when running in V13 ([#929])
- Settings sidebar should now render properly when running in V13 ([#930])


## [1.2.062] - Chimera: Minor Fixes
Fix a few minor bugs.

### Improvements
- Added enchantment target for simple damage bonuses to first damage part ([#924])

### Compendium Content
- Fixed advancement level for Precise Critical & incorrect table name in Font of Magic ([#914])

### Bug Fixes
- Activity selection dialog should now appear when using an item on an lair actor ([#917])
- Non-SVG icons in activity selection dialog should now appear at the proper size ([#918])
- Feature level tag on class journal page should now be properly sorted ([#927])


## [1.2.061] - Chimera: Search Fix
Fix a bug in the search system causing a number of interfaces to no longer function.

### Bug Fixes
- Advancement dialogs that rely on compendium searches will now work again ([#906], [#907])
- Spell list journal pages no longer show only the first spell per collection ([#909])


## [1.2.060] - Chimera: Enricher Improvements
Improvements to enrichers, a new flag for module authors, and more errata changes to the BFRD.

### Improvements
- Check enricher supports multiple proficiencies & linking to activities ([#870], [#901])
- Variable damage types can now be defined in damage enricher without leading key ([#899])
- Added pack flag that allows setting default top-level sorting of compendium packs ([#900])
- Save & check enrichers now support spellcasting ability ([#902])

### Compendium Content
- Applied remaining changes specified in Player's Guide errata to BFRD ([#891])

### Bug Fixes
- Damage enricher should no longer link to activity if damage formula is specified ([#898])


## [1.2.059] - Chimera: Bug Fixes
Fix a few issues with compendium content, initiative modifiers, and property advancement.

### Compendium Content
- Rage bonus should now apply to damage rather than attack, should prompt for application ([#895])
- Prayer of Healing is now marked as a ritual spell ([#896])

### Bug Fixes
- Fixed issue with spell pages when using compendium UUID redirects ([#893])
- Initiative modifiers should now be applied to rolls no matter what button is pressed ([#894])
- Changes should once again appear in `PropertyAdvancement` configuration ([#897])


## [1.2.058] - Chimera: Forward Activity
Adds the Forward activity which allows setting limited uses on spells granted by the *Spells* or *Choose Spells* advancement types.

### Improvements
- Added the ability to specify limited uses when granting spells through advancement ([#765])
- Recovery periods now include "Dawn", "Day", and "Dusk" ([#826])
- New `Forward` activity added for triggering another activity with different consumption ([#888])
- Added the GitHub URL to the system's package manifest ([#890])

### Compendium Content
- Recovery periods on BFRD magic items updated to use new recovery periods ([#826])
- Applied changes specified in Player's Guide errata to BFRD items ([#891])

### Bug Fixes
- Damage rolls will no longer display `undefined` when preparing complex formulas ([#886])
- Heal enricher should no longer throw an error when automatically fetching activity on item with other, non-healing activities ([#887])
- Spells set up on NPCs should now properly set up their consumption when using the NPC spellcasting configuration interface ([#890])
- Blank damage enrichers in activity descriptions should now set activity properly ([#891])


## [1.1.057] - Basilisk: Siege Weapons & Enricher Improvements
Added a new Siege Weapon actor type to support the weapons provided by the Game Master’s Guide and improved the enrichers provided by the system.

### Improvements
- Adjustments to the dimensions of a vehicle now reflects in the prototype token size ([#871])
- Added the Siege Weapon actor type ([#874])
- Damage thresholds are now respected and can by bypassed when applying damage ([#876])
- Improved the localization system for numbers linked to a specific unit ([#877])
- Units for container capacity can now be customized ([#878])
- Enrichers that are linked to activities can now reference a specific activity by ID, rather than just the first matching activity of the correct type ([#880])
- Lookup enricher can now look up activity data from an item ([#881])
- Healing enricher now has `[[/heal]]` alias ([#882])
- Roll build APIs in `BasicRoll` have been made more granular ([#883])
- Renamed `Utility` activity to `Use` to match other activity naming ([#884])
- Configuration parameters for skipping subsequent actions has been added ([#885])


## [1.1.056] - Basilisk: Bug Fixes
A few small bug fixes and improvements to the vehicle actor.

### Improvements
- Bonus Actions & Reactions sections on vehicle sheets now support descriptions ([#872])

### Bug Fixes
- Fixed error generating legendary actions description on NPC sheets ([#867])
- Damage calculation when actor has non-magical damage resistance should work once again ([#868])
- Damage & effect application dropdowns should now render properly in chat ([#875])


## [1.1.055] - Basilisk: Guns & Cars
The first major update the system brings with it vehicles and firearms rules.

### Improvements
- NPC stat blocks can now be embedded using `@Embed[...uuid... statblock]` ([#250])
- Optional firearms rules presented in the GMG can now be enabled in settings ([#832])
- Vehicle actors now supported ([#846])
- Adds module-controlled setting to require custom rules ([#860])

### Bug Fixes
- Fixed several places where item names could cause security issues ([#856])
- Players should now be able to open locked item sheets ([#861])
- Players should now be able to drop items onto the choose features/spell dialog, item sheets, and certain journal sheets ([#862])


## [1.0.054] - Ankheg: Additional Bug Fixes
A few additional bug fixes.

### Bug Fixes
- Fixed error when selecting talent during Improvement ([#857])
- Fixed expertise when applied by talent ([#858])
- Base weapons will no longer display in weapon category list on weapon sheet ([#859])


## [1.0.053] - Ankheg: Bug Fixes & Minor Improvements
Fix a few bugs in the first release and add support for "-" CRs on NPCs.

### Improvements
- NPCs can now have a CR of `-`, which results in an XP value of `0` ([#848])
- Various places in the system now use `DocumentUUIDField` for proper validation ([#851])
- Template count field now supports formulas ([#852])

### Bug Fixes
- "All Damage" resistance, vulnerability, and immunity can now be properly bypasses using the damage application UI ([#663])
- Default variable damage type should now be properly selected if user doesn't interact with damage roll configuration dialog ([#849])
- Documentation link in the Welcome Screen should now display properly in secure contexts ([#850])
- Sheet should no longer minimize/maximize multiple times when placing multiple measured templates ([#853])


## [1.0.052] - Ankheg: Official Release!
The time is upon us! The system is officially emerging from beta. While no longer in beta, the system is still very much in `1.0` status and there are many improvements to come!

### Improvements
- Adjusted damage & healing enrichers to properly handle max HP damage type ([#770])
- Completed removal of minimum uses field ([#815])
- Added Table of Contents application usable by modules ([#833])
- Added Welcome application with links to documentation, the support page, and official ToV modules ([#834])
- Added round time to config so clock increments automatically during combat ([#836])
- Added remaining icons for chat actions ([#837])
- Added identifiers to all item types ([#841])
- Adjusted the text for "Expanded Talent List" in journal pages to match errata text ([#844])
- Luck can now be spent on Death Saves ([#847])

### Compendium Content
- Added UUID redirects from Monster Vault creatures to BFRD versions if Monster Vault isn't enabled ([#845])

### Bug Fixes
- Fixed issues with dark mode on various sheets ([#787])
- Attack mode dropdown will no longer display if no attack modes are available ([#838])
- Half casters & pact casters should now get slots at the correct level ([#839])
- Spell manager & other selection dialogs should no longer display duplicate items ([#840])
- Fixed check enricher failing when requesting a roll ([#843])


## [0.10.051] - Beta: Choice Replacement & Temporary Maximum HP
The system now supports feature & spell replacement on level up and applying temporary changes to maximum HP.

### Improvements
- `Cast` activity is now fully functional ([#328])
- Previously learned spells can now be replaced at level up if allowed by class ([#635])
- Actors now have temporary max HP, Maximum HP healing type now works, and added Maximum HP damage type ([#689])
- Added flag that removes talent list restriction during Improvement ([#761])
- Choose Features & Spells advancement types now support making replacements of earlier choices ([#762])
- Save enricher now supports multiple abilities (from Save activity only) or no ability (using `[[/save ability=false]]`) ([#800])
- Removed "Clothing" gear category and merged subtypes into "Adventuring Gear" and "Wondrous Item" categories ([#821])
- Cast activity can now override the spellcasting ability used for spells ([#824])
- Removed final uses of the deprecated `{% raw %}{{#select}}{% endraw %}` Handlebars helper ([#827])
- Added spell lists journal entry page type ([#828])
- Spellcasting tab now lists more details on spells ([#830])

### Compendium Content
- Update Jack of All Trades to use new `unrestrictedTalents` flag ([#761])
- Updated Path of the Sage to offer spell replacements ([#762])

### Bug Fixes
- Attribute consumption should no longer display "This Item" as a placeholder ([#823])
- Fixed spells being removed when unrelated properties are changed in the Choose Spells configuration ([#829])
- Fixed issue with "All" spell learning mode for non-Divine casters ([#831])


## [0.10.050] - Beta: Completed Reference Doc
The all content from the Black Flag Reference Document is now integrated! This includes all of the monsters and improvements to a number of magic items to take advantage the now functional Summon activity.

### Improvements
- `Summon` activity is now fully functional ([#744])
- Added "Until Destroyed or Dispelled" duration option ([#807])
- Added Circle area of effect type ([#808])
- Bonus modifiers can now increase spellcasting DC ([#810])
- Enchantments now have the ability to apply changes to activities ([#813])

### Compendium Content
- Completed all content from the BFRD ([#497])

### Bug Fixes
- Fixed issue with items that have Consume Quantity set double-counting uses ([#806])
- Fixed active effect suppression on PCs ([#811])
- Automatic consumption scaling should now work for simple negative values ([#812])


## [0.10.049] - Beta: Cast, Summon, & Magic Items Batch 3
Another big batch of magic items, as well as updates to existing items to make use of the new `Cast` activity.

### Improvements
- Added data model & configuration sheet for `Cast` and `Summon` activities ([#328], [#744])
  - **Note**: Neither of these activities are functional yet, but they can be fully configured and will begin working in future releases.
- Added Health configuration application & maximum HP override ([#755], [#793])
- Save activities now support multiple abilities or no ability ([#791], [#799])
- Activation override on activities is now explicitly set ([#794])
- Activities can now trigger a primary action after being activated ([#795])

### Compendium Content
- Magic items up to "Potion of Water Breathing" have been completed ([#497])
- Fixed broken embeds in description of Antipathy/Sympathy spell ([#804])

### Bug Fixes
- Check enrichers using capital letters in key should now be properly parsed ([#796])
- Enrichers without config data should now be recognized ([#797])
- Rolling attack & damage through an enricher in a compendium pack should no be properly prevented ([#798])
- All item types should now be properly be displayed in NPC inventory, but not displayed on main tab ([#801])
- NPC effects should no longer require items to be attuned ([#802])


## [0.10.048] - Beta: Effect Application & Magic Items Batch 2
An interface for applying effects to tokens from activities has been added to chat. Plus continued work on magic items, some improvements to the armor class config, and more!

### Improvements
- Current spell slots can not be changed directly on sheet ([#438])
- Chat cards now display tray for applying effects to tokens ([#697])
- Armor class config has been redesigned and now displays current armor & formulas provided by effects or advancement ([#705])
- Arbitrary actor attributes can now be consumed by activities ([#764])
- List of attributes trackable on the token has been hand-curated ([#785])
- Removed restriction on activity consumption limiting it to a single consumption target for each type ([#786])
- Class & subclass journal pages can now have additional text after the features list ([#789])

### Compendium Content
- Magic items up to "Iron Flask" have been completed ([#497])

### Bug Fixes
- Fix bug preventing rest buttons from working ([#788])
- HitPointsAdvancement should now respect per-level bonuses when updating current HP ([#792])


## [0.10.047] - Beta: Magic Items Batch 1
Added a big chunk of magic items from the reference document, introduced editing mode to item sheets to help with displaying enchanted data, and re-designed the activation dialog to better display consumption amounts.

### Improvements
- Redesigned activation dialog and added consumption preview ([#722], [#778])
- Item sheets now have lock control like actor sheets, toggling between enchanted/not enchanted data ([#756])
- Measured templates can now be placed using guided system ([#760])
- Activity chat cards from spells now display spell circle ([#784])

### Compendium Content
- Source fallback has been removed from BFRD items in favor of automatic detection ([#415])
- Magic items up to "Dragon Scale Mail" have been completed ([#497])

### Bug Fixes
- Save activity DC formula should now be properly migrated ([#768])
- Save activity should now show proper ability in chat card ([#769])
- Luck re-rolls should now properly display on the chat card ([#771])
- Situational terms can once again be applied to attack rolls ([#772])
- XP bar should no longer obscure the actor sheet in certain browsers ([#773])
- Rolling initiative through combat tracker will no longer throw error ([#775])
- Activity & advancement sheets in locked compendiums should now be properly locked ([#776])
- Roll notes should now display on attack rolls ([#777])
- Modifying linked journal entry on concept sheets should no longer discard unsaved description changes ([#779])
- Spellcasting advancement should no longer throw an error when opened from within a compendium ([#780])
- Dragging a feature into the advancement tab of an item should no longer add it again if it already exists ([#781])
- Items without identifiers explicitly set should now be properly registered ([#782])


## [0.10.046] - Beta: Checks, Enchantments, & Templates
A wide mixture of system improvements including base proficiencies (for Jack of All Trades), respecting nonmagical resistances, activities on ammo, the Check activity type, the Enchantment effect type, and guided template placement.

### Improvements
- Base proficiency for checks & saves can now be set ([#129])
- Rich actor & item source can now be configured ([#415])
- Armor class & movement modifiers now receive more details information on equipped armor & shield ([#450])
- Damage enricher now supports variable damage types in explicit and inferred format ([#681])
- Minimum modifiers can now be applied to armor class ([#710])
- Resistances to nonmagical sources of damage are now respected by damage application system ([#727])
- Ammunition items can now have activities & active effects ([#734], [#750])
- Added the Check activity type for making ability, skill, tool, and vehicle checks ([#740])
- Removed restriction requiring both class and background to be present to select starting equipment ([#743])
- Added Enchantment active effect type that applies to items, not actors ([#745])
- Measured templates can now be placed automatically when using activity ([#746])
- String interpolation now supported for active effects in `override` mode ([#751])
- Activities can now be re-ordered on an item ([#752])
- Dropdown in inventory now displays activities and they can be triggered directly from the dropdown ([#757])

### Compendium Content
- Removed level restriction on Mental Fortitude talent ([#739])

### Bug Fixes
- Adding a heal activity will no longer throw an error ([#736])
- NPC damage will no longer add proficiency if ability proficiency checkbox is checked ([#737])
- Critical settings on roll process will now be applied properly to all damage rolls ([#738])
- Luck tray should now display properly for attack rolls ([#742])
- Fixed activity sheets not opening if associated effect is not present ([#749])
- Select equipment dialog should no longer throw error if one item is missing equipment advancement ([#766])
- Item & activity uses consumption on activities should no longer throw an error ([#767])


## [0.10.045] - Beta: Migration Fix
Fix an annoying issue with migrating old activities.

### Bug Fixes
- Old Save & Heal activities should now be properly migrated when inside compendiums ([#735])


## [0.10.044] - Beta: Squashing Bugs
A handful of bug fixes.

### Improvements
- Ammunition dropdown will no longer appear in attack dialog if no ammo is available ([#733])

### Bug Fixes
- Fixed making attacks with weapons that have the Ammunition property if no ammo is present on actor ([#728])
- Description area on Talents should be editable once more ([#729])
- Blank healing enrichers will no longer throw an error ([#730])
- Setting attack ability on Attack activities should work once again ([#731])
- Extra damage parts on weapon attacks should no longer be replaced by copies of the versatile damage ([#732])


## [0.10.043] - Beta: Attack Improvements
It is now possible to make attacks using ammunition and to select attack modes (versatile damage!).

### Improvements
- Methods for wielding weapons (e.g. one-handed, offhand, thrown) can now be selected when making an attack ([#284])
- Resistance/Immunity/Vulnerability to nonmagical damage can now be specified on actors ([#550])
- Activities can now specify whether their effects are magical & whether they require concentration ([#694])
- Custom critical thresholds & bonus damage can now be set on attack activity ([#712])
- Ammunition can now be chosen when attacking & will affect attack & damage rolls ([#714])
- Vehicle checks can now be rolled from enrichers ([#716])
- Attunement requirements can now be specified on items ([#717])
- Activity activation dialog can now by bypassed using "Skip Dialog" keys ([#719])
- Modifiers can now add bonuses to movement ([#725])

### Bug Fixes
- Damage enricher will now roll proper damage when the `versatile` flag is specified ([#695])
- Proficiency bonus no longer removed from NPC attacks ([#704])
- Long rest should once again restore all actor attributes ([#711])
- Fixed advancement & activity sheets not scrolling ([#715])
- Add missing localization for "Skip Dialog" keybindings, fix disadvantage rolling on Mac ([#718])
- Spell slot consumption error message should now properly show spell circle ([#720])
- Consumption labels in activity activation dialog should no longer show raw HTML ([#721])
- Armor items should no longer be listed under NPC features ([#723])
- Choose Features configuration should no longer throw error when pool has items ([#726])


## [0.10.042] - Beta: Spells & Activity Sheets
All of the spells from the BFRD are now set up and ready to be used! Also underwent a redesign of the activity & advancement sheets to make use of the new application framework.

### Improvements
- Utility activity now has a generic roll it can perform ([#584])
- Activities can now declare what specific effects they apply ([#696])
- Migrated activity & advancement sheets to ApplicationV2 ([#698], [#699])
- Moved document type definitions into system manifest ([#703])
- Check enrichers can now be parsed if their include parentheses (so `[[/check INT (Investigation)]]` is now valid) ([#706])
- Renamed `Healing` and `Saving Throw` activities to `Heal` and `Save` ([#707])
- Movement & senses now have units and custom entries ([#708])
- Added `@spellcasting.dc` to roll data ([#709])

### Compendium Content
- Completed all spells in the BFRD ([#497])


## [0.10.041] - Beta: Starting Equipment
Start your characters off with some great gear with the new starting equipment system!

### Improvements
- Added `EquipmentAdvancement` to handle starting equipment & display in class journals ([#62], [#293])
- Activity description tab can now be resized ([#534])
- Roll formulas should now be simplified when displayed in attack enricher ([#675])
- Added overall movement multiplier available through active effects ([#691])
- Calls to `rollSkill` on actors without skills will now forward to `rollAbilityCheck` ([#701])

### Compendium Content
- Added H–I spells ([#497])

### Bug Fixes
- Fixed descriptions sometimes not appearing in activity sheet ([#544])
- Luck UI should once again display in chat messages ([#682])
- Spending luck will no longer cause the chat trays to lose current opened state ([#683])
- Learning spells should no longer delete automatically added spells ([#686])
- Item types without uses should no longer cause the NPC sheet to fail to render ([#688])
- Using short form ability in enrichers (e.g. `[[/save DEX]]`) should now work ([#690])
- Container inventory should now allow expanding items ([#692])
- Rich tooltip styling should no longer affect unrelated tooltips ([#693])
- Formulas in dice numbers should no longer display as `NaN` after being simplified ([#700])
- Various formulas on spells should now be properly resolved ([#702])


## [0.10.040] - Beta: User Experience
A series of user experience improvements are contained in this release, including a new tray for showing attack targets and whether they are hit, a new activity for just doing damage, and reference enrichers for easily linking to rules.

### Improvements
- Display carrying weight on PC sheet & track encumbrance with optional status effects ([#291])
- Introduce `&Reference` enrichers for referencing conditions, damage types, and other rules ([#368])
- Added chat tray indicating whether attack hits targeted tokens ([#430])
- Added rich item tooltips to sheet and spell manager ([#466], [#481])
- Uses scale value can now be infinite and can tie into recovery periods ([#511], [#566])
- Added `DamageActivity` for rolling damage without attack or save ([#666] 👹)
- Added rider conditions that are applied alongside another condition (e.g. unconscious applies prone) ([#667])
- Removed custom active effect application handling that is no longer necessary in V12 ([#671])
- Entries in a set can now be removed by active effects using `-fire` format ([#672])
- Added improved styling for images in journals ([#677])
- Identifiers in scale value advancement config are now copyable, added additional roll paths for dice scale values ([#678])
- Added option for automatically expanding chat trays ([#680])

### Compendium Content
- Added G spells ([#497])
- Added description of psychic damage to the rules ([#670])

### Bug Fixes
- Fixed formatting of embedded roll tables in items to avoid squishing columns ([#665])
- Fixed UUID link in Activity & Advancement headers not matching the modified behavior in V12 ([#668])
- Inline embeds with a label specified should once again show it in front of the embed ([#669])
- NPC sheets should now load properly if a spell without any activities is added ([#676])
- Lair sheets should now load properly if they contain an attack activity, attack activities should now roll properly on lairs ([#679])


## [0.10.039] - Beta: The Big Damage Release
This release brings a laundry list of improvements to how damage is handled in the system. Damage cards have been redesigned in chat to better communicate damage types, activities can now specify variable damage types for spells like Prismatic Wall, and the new damage application interface allows easily applying damage to targets taking resistances, vulnerabilities, and immunities into account.

### Breaking ⚠️
**Foundry V11**: This version drops support for Foundry V11, so you must update to V12 if you want to continue getting new updates to the system.

### Improvements
- Added interface for applying damage from chat cards ([#82], [#105])
- Redesigned damage chat cards to properly communicated damage types ([#280], [#281])
- Activities can now specify a variable damage type that is selectable at usage time ([#402])
- Reworked how items with multiple activities are handled on NPC sheets ([#427])
- Added "All Damage" option for resistances, immunities, and vulnerabilities ([#652])
- Removed V11 compatibility features & backported embeds system ([#656], [#659])
- Redesigned active effects section on items for easier control & more logical grouping ([#660])
- Damage formulas can now specify a number of `0` at the base level so the damage is only applied when upcast ([#661])
- Rebuilt rolling dialogs using Application V2, added support for situational bonuses to each roll ([#662])

### Compendium Content
- Added D–F spells ([#497])

### Bug Fixes
- Fixed active effect icons not appearing in effect list ([#658])
- Fixed naming issue causing lair sheets to not open ([#664])


## [0.9.038] - Beta: Mechanist & More Spells
Harness magical creations with the new Mechanist class and its Metallurgist subclass! This release completes all of the classes offered by the BFRD and also adds all of the spells up through letter C.

### Improvements
- Features can now specify that they can be taken more than once ([#644])
- Activities can now be embedded with an optional activation button ([#645])
- Ritual spells are now scaled based on maximum circle the character can cast ([#647])
- Embedded spells will now display their details in addition to their description ([#648])
- Added the "Wall" area of effect type ([#649])
- Target data no longer defaults to `1` if no area of effect is defined ([#651])
- Items with area of effect defined no longer have to specify specific target in that area ([#653])

### Compendium Content
- Added A–C spells ([#497])
- Added Mechanist class and Metallurgist subclass ([#498])

### Bug Fixes
- Death saves control should once again display properly ([#650])
- Opening item sheet repeatedly will no longer continually scale up base damage die ([#654])
- Average damage calculation should no longer produce `NaN` on V12 ([#655])


## [0.9.037] - Beta: Warlock & Pact Casting
Accept power from beyond with the Warlock class and its Fiend subclass! This release includes Pact Casting and improvements to the system for learning spells.

### Breaking ⚠️
**Spellcasting Ability**: Previously Spellcasting advancement could infer the ability from the selected key ability. With that functionality removed from the Key Ability advancement, each Spellcasting advancement must now define what ability it uses.

### Improvements
- Spell selection now has an option for ritual selection to bypass normal source restriction ([#471])
- Choose Spells advancement can now limit selection to only ritual spells ([#610])
- Pact casting is now available as a spellcasting type ([#622])
- Targeting data can now specify area of effect count and whether the caster chooses targets within the area ([#627])
- Prerequisites can now require another item be present on the actor ([#628])
- Level prerequisite can now reference a specific class level, rather than just character level ([#629])
- Max circle for a specific class is now calculated ([#630])
- Learning spells is now handled by Spellcasting advancement in progression tab, rather than through spellbook ([#631])
- Renamed `system.spellcasting.circles` to `system.spellcasting.slots` to be more accurate ([#636])
- Rest types can now more explicitly define what spellcasting slots are recovered ([#637])
- Spellcasting advancement now requires a specific ability to be defined ([#639])
- Choose Spells advancement can now specify a specific maximum level, in addition to just basing it off the level the character can cast ([#642])

### Compendium Content
- Added Warlock class and Fiend subclass ([#498])
- Set spellcasting ability for each class ([#639])

### Bug Fixes
- Spell selection should no longer allow choosing spells that are of a higher circle then allowed ([#526])
- Layout of Free Spells fields in Spellcasting configuration has fixed ([#632])
- Tables should now be properly styled in Choose Features dialog and item descriptions ([#634])
- Dragging & dropping an advancement onto the same item will no longer duplicate it ([#638])


## [0.9.036] - Beta: Sorcerer & Resource Scaling
Do weird things with your magic in the Sorcerer class and its Draconic subclass! The system now also supports scaling for non-spell features such as a Paladin's Lay on Hands or Sorcerer's ability to trade sorcery points for spell slots.

### Breaking ⚠️
**Saving Throw Proficiencies**: Key Ability advancement no longer grants saving throw proficiency. All of the existing classes has been given a Trait advancement to grant their saving throw proficiencies. Any classes will need to be updated to take this into account including those on actors. Easily update previously created actors by opening the class sheet from the actor's progression tab, then opening the same class in the compendium and dragging the new Saving Throws advancement over to the class on the actor.

### Improvements
- Improved styling and accessibility information on several dialog buttons ([#338])
- Active Effects can now be dragged and dropped ([#397])
- Key Ability advancement now only has one ability selection and no longer grants save proficiency ([#616])
- Non-spell activities can now be scaled and scaling details can be specified for consumption targets ([#617])
- Added "On Short Rest" and "On Long Rest" activation types to support features triggered on rest completion ([#618])
- Removed default actor size to better support features choices that are restricted by size ([#624])

### Compendium Content
- Added additional spells used by new class ([#497])
- Added Sorcerer class and Draconic subclass ([#498])
- Added saving throw proficiencies to classes and updated Key Ability data ([#616])
- Fixed Lay on Hands' "Cure Disease" activity to properly consume uses ([#623])

### Bug Fixes
- Fixed scale value data that was broken by activity scaling data included in roll data ([#620])
- Fixed spell slots not recovering on a long rest ([#626])


## [0.9.035] - Beta: Paladin, Ranger, & Damage Scaling
A twofer this time with the Paladin & Ranger classes with their Devotion & Hunter subclasses! Also, damage scaling can now be configured on spells.

### Improvements
- Spell damage can now be scaled at higher levels ([#439])
- Custom damage formulas are now explicitly toggled ([#613])

### Compendium Content
- Add Paladin & Ranger classes and Devotion & Hunter subclass ([#498])

### Bug Fixes
- Fixed loading new fonts into text editor ([#612])
- Fixed spell slot data being retained on certain actor ([#614])
- Healing rolls should no longer add modifier twice ([#615])


## [0.9.034] - Beta: Monk
Pop pop! The Monk class is here bringing with it the Open Hand subclass!

### Improvements
- Improved legibility of text on low-DPI screens ([#599])
- Refactored Actor & Item data preparation with clearer flow ([#603])
- Activation buttons in actions list will now display activation condition as tooltip ([#607])

### Compendium Content
- Added Monk class & Open Hand subclass ([#498])

### Bug Fixes
- Fixed display of inferred duration & targeting on activity sheets ([#600])
- Fixed styling of content links and inline rolls in certain locations ([#602])
- Upgraded & forced expertise in Trait Advancement should now work with tools & vehicles ([#606])


## [0.9.033] - Beta: Druid
Harness nature's power with the Druid class & Shifter subclass!

### Improvements
- Heading levels in class & subclass journal pages can now be set separate from the indentation level ([#582])
- Improved styling of headers & tables in inventory & chat descriptions ([#588])
- Active effects are now suppressed for items that are not enabled, equipped, or attuned ([#591])
- Features advancement can now add items in a disabled state ([#592])
- Items added through advancement should now get initial sorting values ([#594])
- Features & talents with transferred active effects can now be disabled ([#595])

### Compendium Content
- Updated monster features to take advantage of new system features ([#497])
- Added Druid class & Shifter subclass ([#498])

### Bug Fixes
- Spellcasting values should once again appear in class journal tables ([#589])
- Subclass features should now be grouped under class section in features tab ([#596])
- Items should once again be droppable onto advancement configs ([#598])


## [0.9.032] - Beta: Bard & Lairs
Play some funky music with the Bard class and Lore subclass! There is also a brand new Lair actor to represent the lairs of legendary creatures.

### Improvements
- Added Lair actor and example Red Dragon’s Lair ([#248])
- Added explicit "Spellcasting" save DC option ([#554])
- Added Map Location journal page & custom map markers ([#559])
- Redesigned class & subclass journal page configs ([#562])
- Items can now be posted to chat with descriptions & tags ([#569])
- Creating items directly on actor sheets will now go through the standard Create Item dialog ([#570])
- Added vehicle proficiencies ([#572])
- Embedded features & talents will now display prerequisites ([#573])
- Dropping items directly onto concept advancement tabs will now automatically add to Feature advancement at right level ([#575])
- NPCs now have a source field ([#581])
- Invalid item consumption in activities will now display actor warning ([#586])

### Compendium Content
- Added remaining adventuring gear ([#497])
- Added Bard class & Lore subclass ([#498])
- Updated Backgrounds & Talents to match final BFRD ([#500])

### Bug Fixes
- Badly formatted modifiers should no longer break actor sheets ([#567])
- Fixed un-localized "Any *" labels in trait categories ([#571])
- Advancement data will now be properly cleaned before saving to prevent odd data from being saved ([#574])
- Usage scale value without number will no longer display `null/LR` ([#577])
- Class restriction in advancement list should now display properly ([#580])
- Fixed bug preventing inline rolls in chat message descriptions from rolling ([#585])
- Targeting & duration formulas will now be properly resolved ([#587])


## [0.9.031] - Beta: Barbarian & Talents
Introducing the Barbarian class and Berserker subclass! Plus updated the talent list to match the final BFRD.

### Breaking ⚠️
**NPC Attacks**: NPC attacks without the "Flat" checkbox may have changed due to updated with how proficiency is handled. Existing NPCs should be reviewed to ensure their attacks have the right To Hit.

**Challenge Roll Options**: Critical options passed to roll data have be restructured. This should only matter if you are manually building roll configurations.

### Improvements
- NPCs should now handle proficiency in weapons & other attacks properly ([#442])
- Added support for `min` modifiers on hit dice rolls ([#451])
- Added support for base types on Consumables & Sundry items and added poison consumable type ([#515])
- Class journal page features should now display proper levels regardless of advancement type ([#518])
- Greatly expanded the number of prerequisite options for talents ([#531], [#553], [#555])
- Added `critical-threshold` and `critical-dice` modifiers ([#561])

### Compendium Content
- Updated & added talents to make them match final version of the BFRD ([#497])
- Added Barbarian class & Berserker subclass ([#498])

### Bug Fixes
- Hit Dice & Spell Slot consumption types on non-embedded items should now display selection dropdown ([#556])
- Canceling an initiative roll should no longer throw an error ([#557])
- Activity & Advancement selection dialog title is now localized ([#558])
- Inferred attack type & classification should now be set correctly in Attack activities ([#560])
- Improvement advancement should no longer display warning of action needed if two abilities were selected ([#568])


## [0.9.030] - Beta: NPC Spellcasting
Properly display NPC spellcasting and ensure uses are properly handled. Also added resting support to NPCs to allow spellcasting & other feature uses to recover.

### Improvements
- NPC sheets will now display as multiple columns if made wide enough ([#432])
- NPCs with spells will now get auto-generated spellcasting block with configurable ability & DC ([#441])
- NPCs can now take short and long rests ([#547])
- Spells cast by NPCs will use the ability & DC specified directly on their sheet, unless overridden by the spell ([#548])

### Compendium Content
- Black Flag Rules journals have been updated to match the final BFRD ordering & content ([#497])

### Bug Fixes
- Passive NPC features with activities should now be properly sorted relative to passive features without ([#435])
- System will now use `_stats.compendiumSource` rather than `flags.core.sourceId` in V12 ([#546])
- Properties in chat cards should now wrap ([#549])


## [0.9.029] - Beta: Improved Improvements
Update Improvements to match final rules and support multiple talent lists and fix a number of lingering bugs on V12.

### Improvements
- Portrait can now be edited from top of PC sheet or biography tab ([#490])
- Re-implemented Improvement Advancement to match final released rules ([#503])
- Subclasses will now be auto-populated with feature advancement at the right levels ([#507])
- Spellcasting Value Advancement has been added to represent spells/cantrips/rituals known ([#522])
- Improvement & Expanded Talent List Advancement types can now specify multiple talent lists ([#543])

### Bug Fixes
- Fixed portrait reverting in V12 ([#493])
- More Information links on concept items now work in V12 ([#539])
- Activity config should no longer throw an error in V12 ([#541])
- Inventory & Action sections on sheet should now display proper context menus ([#542])


## [0.9.028] - Beta: Reference Document Lineage & Heritage Updates
Continued updating the content to match the released BFRD and added magical bonuses.

### Improvements
- Weapons, Armor, and Ammunition can now have magical bonuses ([#329], [#345])
- Advancements can now be dragged and dropped ([#527])
- Grant & Choose Spell advancement types can now offer spellcasting ability choice ([#528])

### Compendium Content
- Weapons, armor, and tools have been updated to match released reference document ([#497])
- Lineages & heritages have been updated to match released reference document ([#499])

### Bug Fixes
- Short keys can now be used in enrichers properly (e.g. `dex` instead of `dexterity`) ([#529])
- Clicking "Level Up" without class levels no longer opens ability assignment dialog ([#530])
- Create Actor & Item dialogs now populate folder list when activated from compendiums ([#535])
- Inline text journal page embeds can no include leading label ([#536])
- Trait preparation should no longer fail if invalid traits are found ([#537])


## [0.9.027] - Beta: Activities Improvements
Add duration, range, and targeting to activity data and improve chat cards.

### Improvements
- Activity description, tags, and save DCs are now displayed on chat cards ([#257])
- Added duration, targeting, and range data to activities ([#374])
- Activities can now be added to armor items ([#425])
- GM can now set what save DCs are visible to players ([#429])

### Bug Fixes
- Activity & Advancement sheets should no longer become disconnected from underlying document changes ([#470])
- Now only one sheet for an activity & advancement can be opened at a time ([#521])
- Default activities on activities on various items should now display correctly ([#523])
- Equip button in inventory should now properly fade when not equipped ([#524])
- Saving throws should no longer display incorrect ability on sheet ([#525])


## [0.9.026] - Beta: Reference Document Class Updates
Update existing classes in the system to match released version of reference document and extend them to level 20.

### Improvements
- Custom journal entry sheet added with tweaked styling ([#495])
- Properties have been added to consumables, gear, and tools ([#496])
- Subclass feature levels are now displayed on class journal page ([#506])
- Add new feature types for Heroic & Epic Boons and adjusted sheet logic to better support them ([#509])
- Improvement should now only be listed once on class journal page feature list ([#513])
- Features with scale values now list all their levels in class journal page feature lists ([#514])

### Compendium Content
- Update Cleric, Fighter, Rogue, and Wizard classes to match released reference document ([#497])

### Bug Fixes
- Choose Spells Advancement should now display "Allow Rituals" checkbox at the correct levels ([#501])
- Removed limitation preventing multiple copies of Improvement Advancement from being added ([#505])
- Item categories in Grant Spells Advancement are now properly localized ([#508])
- Change list entries can now be deleted from Property Advancement ([#517])


## [0.9.025] - Beta: Lucky
Luck rest formula can be configured & luck can be decreased.

### Improvements
- The formula used for resetting luck if too much is gained can now be set ([#452])
- Luck can now be removed in editing mode and the explicit value can be set using a config app ([#472])
- Character portrait & token now shown on biography tab ([#482])

### Compendium Content
- Touch of Luck has been updated to set the proper reset formula ([#452])

### Bug Fixes
- Expand and View controls should no longer be disabled on locked sheets ([#478])
- Context menus should now display proper options when accessing documents in locked compendiums ([#479])
- Inventory element no longer prevents hook from being sent out for non-items ([#486])


## [0.9.024] - Beta: Polishing
Fix a few bugs and add multiclassing ability restrictions.

### Improvements
- Multi-classing will now take player's ability scores into account ([#193])

### Bug Fixes
- Content links should now enrich properly in V12 ([#474])
- Spells should now properly choose ability base on their spellcasting origin ([#475])
- Changes to character portrait should now be saved ([#476])


## [0.9.023] - Beta: Spell Advancement
Add Grant & Choose spells advancement types and a few other spell improvements.

### Improvements
- Added `GrantSpellAdvancement` and `ChooseSpellAdvancement` ([#163])
- Always prepared is now a separate boolean value rather than its own preparation mode and preparation data has been moved into the `relationship` flag (**breaking**) ([#465], [#469])
- Spellcasting terminology has been adjusted to match wording in Player's Guide (**breaking**) ([#467])
- Spells can now have short descriptions ([#468])


## [0.9.022] - Beta: Biography & V12 Compatibility
Added biography tab and dropdown descriptions on PC sheets and made the system compatible with Foundry V12.

### Improvements
- Item names on sheet can now be clicked to drop down item description ([#363])
- PCs now have a functional biography tab ([#455])
- Sheet context menus now display in popover rather than inline styling, preventing layout issues ([#456])
- Clicking actor artwork in play mode now pops out a larger version of the image ([#463])

### Compendium Content
- NPCs should now have token artwork properly configured ([#464])

### Bug Fixes
- Compatibility issues with V12 have been fixed ([#458], [#460], [#462])
- Healing activity should no longer throw error when in actions section of PC sheet ([#459])


## [0.8.021] - Alpha 8: Finalize Alpha SRD
Final pass over the Alpha SRD content and squashed a few bugs.

### Improvements
- Identifiers are now set automatically & have an interface for adjustments ([#144], [#145])
- Item resource consumption can now be configured using an UUID for non-embedded items ([#350])
- Level cap has been raised to 20 ([#444])

### Compendium Content
- Complete remaining SRD content ([#167], [#168], [#169], [#170], [#171], [#172], [#174])

### Bug Fixes
- Recovery periods should display properly for activities once more ([#445])
- Resistances & vulnerabilities should now all properly display on PC sheets ([#446])
- Containers within contains in compendiums will no longer throw error generating weight label ([#453])
- Source data on gear items will no longer be squashed to a string ([#454])


## [0.8.020] - Alpha 8: Activation Dialog & Spell Slots
The activation dialog is now implemented allowing for consumption to be bypassed on activation and for selecting a slot to use when casting a spell (no upcasting of damage yet though).

### Improvements
- Legendary actions will now consume uses which will replenish automatically on NPC's turn [#239]
- Activation dialog implemented to allow for configuring consumption & other usage [#263]
- NPC features will now display their limited uses on the main tab [#369]
- Uses can now be recharged based on a D6 roll which will be rolled automatically [#376]

### Compendium Content
- Monsters compendium now completed ([#326])

### Bug Fixes
- Casting spells will now actually consume spell slots ([#335])
- Damage dialog & chat card will now properly display healing types ([#436])
- Spells slots now properly recover during rests ([#437])
- Remaining legendary actions can now be properly edited on NPC sheet ([#440])


## [0.8.019] - Alpha 8: Complete NPCs
Add a number of features to make building NPC stat blocks easier and more rich.

### Improvements
- Legendary actions can now be added to NPC sheets ([#239])
- Add "Add Feature" button to NPC main tab & create features with Monster type by default ([#321], [#372])
- To hit value on attacks can now have bonus & flat value ([#370])
- GMs can now send check/save enricher rolls to chat ([#411])
- Abilities on check/save enrichers will now display as capitalized acronym to match official books ([#417])
- Empty save enricher will now fetch values from a Saving Throw activity ([#418])
- NPC sheets will now display activities with "Free Action" activation in passive section ([#419])
- Actions list now has a context menu ([#421])
- Blank damage enricher can now display versatile damage on weapons ([#424])
- New healing enricher added ([#426])
- Localized reach & range labels can now be referenced using lookup enricher ([#433])

### Compendium Content
- Added icons and standard descriptions to SRD weapons ([#174])
- Continue building out SRD monsters ([#326])

### Bug Fixes
- Switching sheet mode will now commit unsaved changes ([#416])
- Blank damage enrichers should no longer throw an error if one of the damage lines has a blank formula ([#420])
- Blank damage enrichers should now properly include base weapon damage ([#422])
- Prevent NPC weapon attacks from adding proficiency ([#423])
- Blank enrichers on activity descriptions should now fetch proper data if more than one activity is present ([#428])
- Blank healing enricher should now properly fetch and roll ([#434])


## [0.8.018] - Alpha 8: Additional Spell Improvements
Completed features for learning spells and expanded enrichers to aid with creation of template monster features.

### Improvements
- Added `[[/attack]]` enricher for rolling attacks ([#247])
- Source data is now object to support more rich source details ([#302])
- Spells & physical items now have an effects tab ([#360])
- "Self" label has been removed from blank targets, blank target now allowed for areas of effect ([#401])
- Learning spells can now be restricted by school & a special 1st-level slot can be designated ([#404], [#405])
- Mechanism linking cantrips/rituals/spells known scale values to spellcasting advancement has been simplified ([#408])
- Enrichers can now roll from multiple tokens at once ([#410])
- Damage enricher now supports multiple parts & damage derived from containing item ([#412], [#413])

### Compendium Content
- Added artwork for SRD monsters ([#326])

### Bug Fixes
- Activity description editor will no longer lose the description ([#414])


## [0.8.017] - Alpha 8: Bug Fix
Fix a bug with the spell manager & add a new notification.

### Improvements
- Sheet now displays notification after leveling up if new spells need to be learned ([#403])

### Bug Fixes
- Spell manager should no longer throw error when viewing ring slot ([#407])


## [0.8.016] - Alpha 8: Learning Spells
Adds a spell manager that support learning spells based on class or subclass's spellcasting details. This allows clerics and druids to gain all spells for their circle they can cast, sorcerers and spell blades can choose a certain number of spells, and wizards can scribe some free spells into their spellbook.

### Improvements
- Implemented system for learning new spells at each level ([#160])
- Added spellcasting source block to spellbook tab that displays ability, to hit, save DC, & prepared spells ([#347])
- Adjusted movement & sense tags to be associated with specific block ([#383])
- Custom creature type tags can now be added ([#387])
- NPC sheets will now show adjusted stealth from noisy armor ([#390])
- Players will now get a roll note indicating they have disadvantage on stealth with noisy armor ([#406])

### Compendium Content
- SRD spells have now all been added ([#173])

### Bug Fixes
- Roll notes should once again properly display ([#400])


## [0.8.015] - Alpha 8: SRD NPC Stats
Began implementing all the NPCs in the SRD (attributes, but no features) and improved a number of things on the NPC sheet.

### Improvements
- Implemented `[[lookup]]` and `[[calc]]` enrichers for stock NPC features ([#276], [#398])
- Custom armor labels can now be set ([#364])
- Senses & movement now have tags ("Can't sense beyond this radius" & "Hover") ([#380])
- Creature tags are now implemented ("Animal", "Shapechanger", etc.) ([#381])
- Added Druidic & Thieves' Cant under "Secret Languages" category ([#389])
- Vulnerable, Resistant, and Immune sections on NPC sheets now formatted to match SRD presentation ([#393])
- Added condition vulnerabilities ([#395])
- Effects tab on actor sheets has been redesigned to match inventory styling ([#396])

### Compendium Content
- Built out stats for all NPC monsters, added several NPC features ([#326])

### Bug Fixes
- Resistance config no longer shows traits applied by active effects as checked ([#382])
- Fixed column highlighting on Resistance configuration dialog ([#384])
- Key for lightning damage is no longer misspelled ([#385])
- Resistances now actually display on NPC sheets ([#386])
- Minimized NPC sheets now display the actor name ([#388])
- Standard languages are now sorted before Esoteric languages ([#391])
- Fixed document ID button in header of NPC sheets not functioning ([#392])
- Grandchild effects can now be interacted with on actor sheets ([#394])
- Implicit NPC perception & stealth values are now prepared in derived data, rather than sheet context ([#399])


## [0.8.014] - Alpha 8: SRD Improvements
Build out all of the journals that will be part of the SRD with the new Rule page.

### Improvements
- Spells can now have multiple circles ([#337])
- Activities on NPC sheets now fall back to item description ([#373])
- Refactored rolling infrastructure to have clearer API ([#377])
- Added rule journal entry page type ([#378])

### Compendium Content
- Journals for SRD rules built out ([#175])

### Bug Fixes
- NPC should now have the proper proficiency calculated ([#371])
- Item on NPC main page are now properly sorted ([#375])


## [0.8.013] - Alpha 8: Spellcasting Improvements
Some new information added to the spells tab for each spellcasting source and max slots can be manually changed.

### Improvements
- Each spellcasting source now displays details block at top of spells tab ([#347])
- Spellcasting advancement can now define alternate spellcasting ability, rather than only getting Key Ability ([#355])
- Max spell slots can no be overridden for each ring ([#359])

### Bug Fixes
- Advancements on subclasses no longer display class restrictions ([#352])
- Cantrips/Rituals/Spells known scale values created from Spellcasting Advancement will now have correct type ([#353])
- Advancement notifications once again display their messages ([#356])
- Notification to select subclass will now only appear on correct class's block ([#357])
- Auto-created advancements on concept items will now call `_preCreate` ([#361])


## [0.8.012] - Alpha 8: Rarity & Gear
Added rarities to items and more SRD content.

### Improvements
- Added adventuring gear and magic items ([#174])
- Items can now have rarities ([#344])
- Warning will now be displayed if too many items are attuned ([#346])

### Bug Fixes
- Previously chosen languages will no longer be presented as valid options ([#334])
- Rolling ability scores out of order will no longer cause an error ([#348])


## [0.8.011] - Alpha 8: Accessibility & Inventory Improvements
Modify the sheet to be more accessible, add controls for attuning & equipping items and preparing spells.

### Improvements
- Spells can now be prepared and filtered by prepared status ([#154])
- Items can now be attuned and attunement count is displayed in inventory ([#327])
- Concept items now have extended description on item ([#331])
- Set Property & Size advancement types now have hints ([#332])
- Replaced old SVG caching system with `<blackFlag-icon>` elements ([#336])
- Items added by other items added by classes will now be grouped with the proper class ([#339])
- Added system branding to setup screen, login screen, and settings sidebar ([#340])
- Physical items are now equipped, rather than enabled ([#341])
- Added more controls button to bring up context menu in inventory ([#342])
- Redesigned enabled checkbox on features to match equipped & other controls ([#343])

### Bug Fixes
- Class selection dialog can now be scrolled in Chrome ([#333])


## [0.7.010] - Alpha 7: Bug Fixes & NPC Improvements
Add the final pieces necessary for functional NPCs and fix a variety of bugs.

### Improvements
- Added application for manually configuring weapon & armor proficiencies ([#117])
- Added ability to manually set base ability scores from the config app if allowed by the setting ([#118])
- Added application for configuring languages & language tags ([#272])
- Added perception, stealth, & initiative to NPC sheets, improved fractional CRs ([#274])
- Token size will now automatically update to match changes to actor size ([#309])
- Short & long rest buttons now exist within the PCs action list ([#310])
- `@Embed` enricher now functions the same as the upcoming V12 version ([#315])
- Advancement & Activity configs now have a button for copying ID & UUID like core documents ([#316])
- Languages are now grouped into "Standard" and "Esoteric" categories, with "Primordial" dialects ([#318])
- Reworked `groupedSelectOptions` to avoid nested `<optgroup>` elements ([#319])
- Added support for telepathy & custom languages ([#320])
- NPC abilities can now be rolled directly from the sheet ([#324])
- Added support for condition resistances ([#325])

### Bug Fixes
- Delete journal link button should not longer display on locked items ([#311])
- Death saves icon should no longer be transparent in Chrome ([#312])
- Concept can now be deleted from the progression tab ([#314])
- Usage scale values should now be able to have their "per" value unset properly ([#317])
- Activities should no longer show the "Roll Damage" button if no damage is configured ([#323])


## [0.7.009] - Alpha 7: UI Polish
A few polishing updates.

### Improvements
- Actors & items now have a variety of default icons ([#103])
- Blocks on PC sheet moved around to give more room to actions & remove excessive white space ([#138])
- PC token link & disposition will now be set on creation ([#147])


## [0.7.008] - Alpha 7: Mundane Items
Add the remaining item types, containers that can hold items, and rework conditions.

### Improvements
- Items are now enabled by default when added to actors ([#282])
- `Container`, `Consumable`, `Gear`, `Tool`, and `Sundry` item types added ([#288], [#289], [#294], [#295], [#296], [#301])
- Added `Currency` item type and currency section in inventory ([#290], [#306])
- Refactored drag & drop code to live inside `InventoryElement` ([#298])
- Refactored conditions to apply changes on data preparation rather than using active effects ([#299], [#300])
- Build scripts now output compendium sources into folders ([#303])
- Items now have the option to consume quantities when they run out of uses ([#305])

### Bug Fixes
- Fix drag event working incorrectly in Chromium browsers ([#297])
- Fix bug calculating weight using mixed units ([#308])


## [0.6.007] - Alpha 6: Polish
A polish release that improves various inventory tabs, damage application, and critical damage. Also adds a few new activity types.

### Improvements
- `applyDamage` method now takes resistance, immunity, and vulnerability into account ([#53])
- Luck cards in chat now update when luck is spent or gained ([#72])
- Features, inventory, & spellcasting tabs can now be automatically sorted ([#83])
- Actions for non-enabled items are now automatically hidden ([#84])
- Base weapon, armor, & tool choices are now properly filtered ([#88])
- Maximize critical dice & multiply dice critical options added ([#106])
- Tools can now be configured from the sheet ([#137])
- Spellcasting tab can now be filtered ([#153], [#286])
- `HealingActivity` and `UtilityActivity` added ([#229], [#230])
- Activities can now customize activation costs ([#262])
- Items can now be created directly on actor sheets ([#275])
- Saving throw no longer allows critical damage ([#283])
- Spellcasting tab now has "Ritual", "Innate", and "At Will" sections ([#285])
- Activities can now be dragged and dropped between items ([#287])


## [0.6.006] - Alpha 6: Opponents
NPCs can now be created to oppose players and limited uses have been added to items & activities.

### Improvements
- Activities can now be added to features & talents ([#228])
- `NPC` actor type added ([#233], [#236], [#237], [#238])
- Added support for limited uses ([#235])
  - Added limited uses pools to items & activities ([#240], [#241], [#243], [#261])
  - Added support for complex use recovery ([#242], [#260])
  - Display uses in inventory & actions lists ([#258], [#264])
- Several new enrichers can now be used ([#244])
 - [#227]: `&embed` enricher added for embedding journal pages or advancement features
 - [#245]: `[[/damage]]` enricher added for rolling damage using built-in damage rolls
 - [#246]: `[[/save]]` and `[[/check]]` enrichers added for rolling using a selected actor
- Added creature types to PCs and NPCs ([#249])
- Ability can now be specified on `AttackActivity` ([#251])
- Improved how damage entries can be customized ([#253], [#255], [#256])
- Custom elements added for damage lists & inventory ([#254], [#259], [#266])
- Now actions are displayed in list on PC sheet based on activities ([#264])
- Improved design of tabs for better clarity ([#267])
- Class features will now be grouped by class on the PC sheet ([#268])
- Implemented new `MovementConfig` and `SensesConfig` apps for actors ([#270], [#271])
- Activities can now have descriptions ([#273])

### Bug Fixes
- Features without types should now display properly on features tab ([#265])


## [0.5.005] - Alpha 5: Beyond 1st Level
Characters can now be leveled up, select subclasses when they reach 3rd level, and improvements at 4th level. When leveling up they also have the option of multi-classing, if the DM allows it. This release also includes the initial version of the activities system, so you can make attacks with weapons and spells.

### Improvements
- Adjusted `ChooseFeaturesDialog` to add restrictions, browsing all compendium items ([#31])
- Improved class journal pages ([#65])
  - Subclass & improvement will now display in progression table & feature list ([#63])
  - Class pages can now display a list of associated subclasses ([#220])
  - Scale values on features will now display grouped with those features in the table ([#219], [#222])
  - Features will now display descriptive tag (e.g. "5th-Level Rogue Feature") ([#221])
- Implemented activities system ([#80], [#96], [#97], [#100])
  - Implemented `AttackActivity` & will now create it automatically on new weapons ([#98], [#101])
  - Implemented `SavingThrowActivity` ([#99])
  - Added support for activities on spells ([#156])
- Updated underlying architecture of advancements to be built on new PseudoDocument architecture ([#104])
- Features can now be associated with a specific class, lineage, or heritage ([#176])
- Characters can now take multiple classes ([#189])
  - Advancement system has been improved to support multi-classing ([#165], [#190], [#191], [#192])
  - Designed level-up interface which allows selecting existing class or multi-classing ([#194])
  - HP calculation now takes different classes into account ([#206])
  - Added system setting to disable multi-classing ([#215])
- `Subclass` item type added ([#187], [#207], [#208])
  - Added interface for selecting subclass at 3rd level ([#188])
  - Created subclasses in SRD ([#204])
  - Subclasses will now be displayed grouped with classes on progression screen ([#209], [#210])
  - Adjusted advancement types so they can be used on subclasses ([#211], [#213])
  - Added `ExpandedTalentList` advancement for subclasses ([#212])
  - Added subclasses to class journal page & they get their own journal page ([#216])
- Changed progression screen from tab to separate mode to prevent excessive rendering of advancement flows ([#195])
- Improved the experience of leveling up ([#196])
  - Styling of level up controls on progression tab improved ([#197])
  - XP bar added to progression tab is leveling setting is set to XP ([#198], [#199])
- Added `ImprovementAdvancement` ([#200], [#201], [#202], [#203])
- World documents will no longer appear in registered items lists ([#214])
- Moved contained sheet logic into custom elements ([#224], [#225])
- Added context menu options for edit, duplicate, toggle, and delete commands for active effects ([#226])

### Bug Fixes
- Hit dice should now disappear from sheet if no class with that HD size remains ([#185])
- Fix single level advancements not having their level properly set on creation ([#217])
- Sheet should now re-render when adding class with no advancement on initial level ([#218])


## [0.4.004] - Alpha 4: Spellcasting
Introduces the spellcasting system and spell items. Classes can get spellcasting progression and the number of slots per ring will be calculated automatically.

### Improvements
- Death saves can now be rolled with player reaches zero HP ([#78], [#79])
- Implement spellcasting system ([#148])
  - Added `SpellcastingAdvancement` to represent a class's spellcasting abilities ([#150], [#157], [#158], [#161])
  - Actors now calculate spell slots/rings based on spellcaster level ([#151])
  - Class journal pages will now display spellcasting progression in table ([#61])
- `Spell` item type added ([#149])
- Spellcasting tab on character sheets now displays spells ([#152])
- Implemented `ScaleValueAdvancement` ([#162], [#177], [#178], [#179], [#180])
  - Class journal pages will now display scale values in table ([#64])
  - SRD classes now have scale values configured ([#182])
- [#154] Features & talents can now be restricted by spellcasting
- Advancements will now have confirmation prompt when being deleted ([#166])


## [0.3.003] - Alpha 3: Combat
Added weapons & armor, armor class calculations, condition tracking, and initiative.

### Improvements
- `TraitAdvancement` has been improved ([#69])
  - Choices can now be set to use "exclusive" selection mode ([#29])
  - Build proficiencies section on class journal pages ([#66])
  - Non-valid checkboxes will now be disabled when group or wildcard options selected ([#70])
  - Wildcard checkboxes are now styled distinctly ([#71])
  - Choice description is now displayed on progression tab and is customizable ([#92])
  - Invalid choices are removed when changed to one of the expertise modes ([#93])
  - Configuration window will now more logically shift to correct trait type ([#94])
- `Weapon`, `Ammunition`, & `Armor` item types added ([#74], [#75], [#76])
- Condition system implemented ([#77])
  - Condition item type added with associated effects ([#139], [#140])
  - Core status effects have been replaced with system-specific ones ([#141], [#142])
  - Conditions can now be set from the effects tab on PC sheets ([#143])
  - SRD conditions added to system compendium ([#146])
- Created `DamageRoll` roll type ([#81])
  - Damage rolls display in chat with damage types & total across multiple rolls ([#107])
- Lineage features now contains "Natural Adaptation" type ([#86])
- Method for declaring data models moved entirely into config ([#89])
- Journal headers now use custom typeface ([#90])
- Physical items can now be equipped ([#91])
  - Equipped status and other relationship data will be automatically cleared when item is moved ([#115])
- Cached SVG images now use <def> references, rather than repeating the whole SVG ([#95])
- Made PseudoDocument system for advancement/activities ([#96])
- Implemented armor class ([#108])
  - Armor class is now calculated automatically using a set of formulas ([#87])
  - Modifiers can now be used to add bonus to armor class ([#109])
  - Armor class configuration app added for configuring formulas & override ([#110])
  - Roll note will be created automatically if wearing non-proficient armor ([#111])
  - Warning will be displayed if more than one armor or shield is used ([#112])
- Proficiency will now be calculated automatically for armor & weapons ([#113])
- All trait proficiencies are now displayed on sheet ([#116])
- Implemented initiative ([#121])
  - Core initiative rolling now uses system-specific formula ([#122])
  - Initiative configuration app added with controls for selecting ability & proficiency ([#123])
  - Modifiers can now be used to add bonus, minimums, and notes to initiative ([#124])
  - Initiative styling improved on sheet & can now be rolled directly ([#125], [#126])
  - Initiative dialog will now be displayed when rolling from combat tracker ([#127])
  - Using luck on initiative rolls now effects order in combat tracker ([#128])
- Tool checks can now be rolled from sheet ([#130])
- Styling on tool and skill sections is improved ([#133])

### Bug Fixes
- Chat messages should still render if referenced actor has been deleted ([#73])
- Progression tab should now retain scroll position when choices are made ([#85])


## [0.2.002] - Alpha 2: Checks & Luck
Implemented ability checks & saves, luck, roll modifiers, resting, and a journal entry page for classes.

### Improvements
- Talents & features now support pre-requisites that are enforced by the choose Features advancement ([#32])
- `BaseRoll`, `ChallengeRoll`, and `ChallengeDie` added to support dice rolls ([#33])
- Player can now roll ability checks, ability saves, and skill checks ([#34])
- System of roll modifiers to add bonuses, set minimums, and indicate advantage implemented ([#36], [#40], [#47], [#58])
- Luck system implemented with ability to add luck on sheet & spend on d20 rolls from chat ([#37], [#38], [#39])
- HP & temp HP can now be managed from character sheet ([#41])
- PCs can now take short and long rests, rolling hit dice & recovering them along with HP as appropriate ([#42], [#54])
- New class, background, lineage, and heritage items will now have standard advancement created automatically ([#43])
- Add journal page sheet type that automatically generates a class summary ([#45])
- Highlight roll results (success/failure & criticals) in roll messages ([#46])
- Data models now use mixin pattern for more extensibility ([#59])

### Bug Fixes
- Registration should no longer throw error when updating multiple documents ([#51])
- Choose Features dialog should still display if linked items cannot be located ([#52])
- Font Awesome Pro icons will no longer be used by accident for dice icons ([#55])


## [0.1.001] - Alpha 1: Character Creation
Character creation workflow created with classes, lineages, heritages, and backgrounds as well as features and talents. The progression tab was built to display these choices and an interface was added to help select these concept items and ability scores.

### Improvements
- Advancement system derived from dnd5e & Everyday Heroes implemented ([#6], [#15])
- Designed character progression tab to store details on character concept, levels, & choices ([#7], [#17], [#28])
- `Class`, `Lineage`, `Heritage`, & `Background` item types added ([#8], [#9], [#10], [#11])
- Registration system implemented to pre-load details on concept items ([#12])
- Concept items can now be selected from list & only one of each type can be added ([#13], [#26])
- Designed interface for selecting initial ability scores ([#14])
- Character sheet has been localized & the design improved ([#18], [#21])
- Feature & Talent item types added ([#19], [#20], [#30])
- Info & warning system has been added to character sheet to guide character creation process ([#22])
- `KeyAbilityAdvancement` added for classes to grant save proficiency ([#23])
- `SizeAdvancement` added for lineages to select creature size ([#24])
- `TraitAdvancement` added to give skills, languages, & proficiencies ([#25])
- `PropertyAdvancement` added to set arbitrary properties ([#27])


## Pre-alpha
- Set up project structure & build scripts ([#1], [#2])
- Build basic data structure for PCs & base character sheet ([#3])


[0.1.001]: https://github.com/koboldpress/black-flag/releases/tag/0.1.001
[0.2.002]: https://github.com/koboldpress/black-flag/releases/tag/0.2.002
[0.3.003]: https://github.com/koboldpress/black-flag/releases/tag/0.3.003
[0.4.004]: https://github.com/koboldpress/black-flag/releases/tag/0.4.004
[0.5.005]: https://github.com/koboldpress/black-flag/releases/tag/0.5.005
[0.6.006]: https://github.com/koboldpress/black-flag/releases/tag/0.6.006
[0.6.007]: https://github.com/koboldpress/black-flag/releases/tag/0.6.007
[0.7.008]: https://github.com/koboldpress/black-flag/releases/tag/0.7.008
[0.7.009]: https://github.com/koboldpress/black-flag/releases/tag/0.7.009
[0.7.010]: https://github.com/koboldpress/black-flag/releases/tag/0.7.010
[0.8.011]: https://github.com/koboldpress/black-flag/releases/tag/0.8.011
[0.8.012]: https://github.com/koboldpress/black-flag/releases/tag/0.8.012
[0.8.013]: https://github.com/koboldpress/black-flag/releases/tag/0.8.013
[0.8.014]: https://github.com/koboldpress/black-flag/releases/tag/0.8.014
[0.8.015]: https://github.com/koboldpress/black-flag/releases/tag/0.8.015
[0.8.016]: https://github.com/koboldpress/black-flag/releases/tag/0.8.016
[0.8.017]: https://github.com/koboldpress/black-flag/releases/tag/0.8.017
[0.8.018]: https://github.com/koboldpress/black-flag/releases/tag/0.8.018
[0.8.019]: https://github.com/koboldpress/black-flag/releases/tag/0.8.019
[0.8.020]: https://github.com/koboldpress/black-flag/releases/tag/0.8.020
[0.8.021]: https://github.com/koboldpress/black-flag/releases/tag/0.8.021
[0.9.022]: https://github.com/koboldpress/black-flag/releases/tag/0.9.022
[0.9.023]: https://github.com/koboldpress/black-flag/releases/tag/0.9.023
[0.9.024]: https://github.com/koboldpress/black-flag/releases/tag/0.9.024
[0.9.025]: https://github.com/koboldpress/black-flag/releases/tag/0.9.025
[0.9.026]: https://github.com/koboldpress/black-flag/releases/tag/0.9.026
[0.9.027]: https://github.com/koboldpress/black-flag/releases/tag/0.9.027
[0.9.028]: https://github.com/koboldpress/black-flag/releases/tag/0.9.028
[0.9.029]: https://github.com/koboldpress/black-flag/releases/tag/0.9.029
[0.9.030]: https://github.com/koboldpress/black-flag/releases/tag/0.9.030
[0.9.031]: https://github.com/koboldpress/black-flag/releases/tag/0.9.031
[0.9.032]: https://github.com/koboldpress/black-flag/releases/tag/0.9.032
[0.9.033]: https://github.com/koboldpress/black-flag/releases/tag/0.9.033
[0.9.034]: https://github.com/koboldpress/black-flag/releases/tag/0.9.034
[0.9.035]: https://github.com/koboldpress/black-flag/releases/tag/0.9.035
[0.9.036]: https://github.com/koboldpress/black-flag/releases/tag/0.9.036
[0.9.037]: https://github.com/koboldpress/black-flag/releases/tag/0.9.037
[0.9.038]: https://github.com/koboldpress/black-flag/releases/tag/0.9.038
[0.10.039]: https://github.com/koboldpress/black-flag/releases/tag/0.10.039
[0.10.040]: https://github.com/koboldpress/black-flag/releases/tag/0.10.040
[0.10.041]: https://github.com/koboldpress/black-flag/releases/tag/0.10.041
[0.10.042]: https://github.com/koboldpress/black-flag/releases/tag/0.10.042
[0.10.043]: https://github.com/koboldpress/black-flag/releases/tag/0.10.043
[0.10.044]: https://github.com/koboldpress/black-flag/releases/tag/0.10.044
[0.10.045]: https://github.com/koboldpress/black-flag/releases/tag/0.10.045
[0.10.046]: https://github.com/koboldpress/black-flag/releases/tag/0.10.046
[0.10.047]: https://github.com/koboldpress/black-flag/releases/tag/0.10.047
[0.10.048]: https://github.com/koboldpress/black-flag/releases/tag/0.10.048
[0.10.049]: https://github.com/koboldpress/black-flag/releases/tag/0.10.049
[0.10.050]: https://github.com/koboldpress/black-flag/releases/tag/0.10.050
[0.10.051]: https://github.com/koboldpress/black-flag/releases/tag/0.10.051
[1.0.052]: https://github.com/koboldpress/black-flag/releases/tag/1.0.052
[1.0.053]: https://github.com/koboldpress/black-flag/releases/tag/1.0.053
[1.0.054]: https://github.com/koboldpress/black-flag/releases/tag/1.0.054
[1.1.055]: https://github.com/koboldpress/black-flag/releases/tag/1.1.055
[1.1.056]: https://github.com/koboldpress/black-flag/releases/tag/1.1.056
[1.1.057]: https://github.com/koboldpress/black-flag/releases/tag/1.1.057
[1.2.058]: https://github.com/koboldpress/black-flag/releases/tag/1.2.058
[1.2.059]: https://github.com/koboldpress/black-flag/releases/tag/1.2.059
[1.2.060]: https://github.com/koboldpress/black-flag/releases/tag/1.2.060
[1.2.061]: https://github.com/koboldpress/black-flag/releases/tag/1.2.061
[1.2.062]: https://github.com/koboldpress/black-flag/releases/tag/1.2.062
[1.3.063]: https://github.com/koboldpress/black-flag/releases/tag/1.3.063

[#1]: https://github.com/koboldpress/black-flag/issues/1
[#2]: https://github.com/koboldpress/black-flag/issues/2
[#3]: https://github.com/koboldpress/black-flag/issues/3
[#6]: https://github.com/koboldpress/black-flag/issues/6
[#7]: https://github.com/koboldpress/black-flag/issues/7
[#8]: https://github.com/koboldpress/black-flag/issues/8
[#9]: https://github.com/koboldpress/black-flag/issues/9
[#10]: https://github.com/koboldpress/black-flag/issues/10
[#11]: https://github.com/koboldpress/black-flag/issues/11
[#12]: https://github.com/koboldpress/black-flag/issues/12
[#13]: https://github.com/koboldpress/black-flag/issues/13
[#14]: https://github.com/koboldpress/black-flag/issues/14
[#15]: https://github.com/koboldpress/black-flag/issues/15
[#17]: https://github.com/koboldpress/black-flag/issues/17
[#18]: https://github.com/koboldpress/black-flag/issues/18
[#19]: https://github.com/koboldpress/black-flag/issues/19
[#20]: https://github.com/koboldpress/black-flag/issues/20
[#21]: https://github.com/koboldpress/black-flag/issues/21
[#22]: https://github.com/koboldpress/black-flag/issues/22
[#23]: https://github.com/koboldpress/black-flag/issues/23
[#24]: https://github.com/koboldpress/black-flag/issues/24
[#25]: https://github.com/koboldpress/black-flag/issues/25
[#26]: https://github.com/koboldpress/black-flag/issues/26
[#27]: https://github.com/koboldpress/black-flag/issues/27
[#28]: https://github.com/koboldpress/black-flag/issues/28
[#29]: https://github.com/koboldpress/black-flag/issues/29
[#30]: https://github.com/koboldpress/black-flag/issues/30
[#31]: https://github.com/koboldpress/black-flag/issues/31
[#32]: https://github.com/koboldpress/black-flag/issues/32
[#33]: https://github.com/koboldpress/black-flag/issues/33
[#34]: https://github.com/koboldpress/black-flag/issues/34
[#36]: https://github.com/koboldpress/black-flag/issues/36
[#37]: https://github.com/koboldpress/black-flag/issues/37
[#38]: https://github.com/koboldpress/black-flag/issues/38
[#39]: https://github.com/koboldpress/black-flag/issues/39
[#40]: https://github.com/koboldpress/black-flag/issues/40
[#41]: https://github.com/koboldpress/black-flag/issues/41
[#42]: https://github.com/koboldpress/black-flag/issues/42
[#43]: https://github.com/koboldpress/black-flag/issues/43
[#45]: https://github.com/koboldpress/black-flag/issues/45
[#46]: https://github.com/koboldpress/black-flag/issues/46
[#47]: https://github.com/koboldpress/black-flag/issues/47
[#51]: https://github.com/koboldpress/black-flag/issues/51
[#52]: https://github.com/koboldpress/black-flag/issues/52
[#53]: https://github.com/koboldpress/black-flag/issues/53
[#54]: https://github.com/koboldpress/black-flag/issues/54
[#55]: https://github.com/koboldpress/black-flag/issues/55
[#58]: https://github.com/koboldpress/black-flag/issues/58
[#59]: https://github.com/koboldpress/black-flag/issues/59
[#61]: https://github.com/koboldpress/black-flag/issues/61
[#62]: https://github.com/koboldpress/black-flag/issues/62
[#63]: https://github.com/koboldpress/black-flag/issues/63
[#64]: https://github.com/koboldpress/black-flag/issues/64
[#65]: https://github.com/koboldpress/black-flag/issues/65
[#66]: https://github.com/koboldpress/black-flag/issues/66
[#69]: https://github.com/koboldpress/black-flag/issues/69
[#70]: https://github.com/koboldpress/black-flag/issues/70
[#71]: https://github.com/koboldpress/black-flag/issues/71
[#72]: https://github.com/koboldpress/black-flag/issues/72
[#73]: https://github.com/koboldpress/black-flag/issues/73
[#74]: https://github.com/koboldpress/black-flag/issues/74
[#75]: https://github.com/koboldpress/black-flag/issues/75
[#76]: https://github.com/koboldpress/black-flag/issues/76
[#77]: https://github.com/koboldpress/black-flag/issues/77
[#78]: https://github.com/koboldpress/black-flag/issues/78
[#79]: https://github.com/koboldpress/black-flag/issues/79
[#80]: https://github.com/koboldpress/black-flag/issues/80
[#81]: https://github.com/koboldpress/black-flag/issues/81
[#82]: https://github.com/koboldpress/black-flag/issues/82
[#83]: https://github.com/koboldpress/black-flag/issues/83
[#84]: https://github.com/koboldpress/black-flag/issues/84
[#85]: https://github.com/koboldpress/black-flag/issues/85
[#86]: https://github.com/koboldpress/black-flag/issues/86
[#87]: https://github.com/koboldpress/black-flag/issues/87
[#88]: https://github.com/koboldpress/black-flag/issues/88
[#89]: https://github.com/koboldpress/black-flag/issues/89
[#90]: https://github.com/koboldpress/black-flag/issues/90
[#91]: https://github.com/koboldpress/black-flag/issues/91
[#92]: https://github.com/koboldpress/black-flag/issues/92
[#93]: https://github.com/koboldpress/black-flag/issues/93
[#94]: https://github.com/koboldpress/black-flag/issues/94
[#95]: https://github.com/koboldpress/black-flag/issues/95
[#96]: https://github.com/koboldpress/black-flag/issues/96
[#97]: https://github.com/koboldpress/black-flag/issues/97
[#98]: https://github.com/koboldpress/black-flag/issues/98
[#99]: https://github.com/koboldpress/black-flag/issues/99
[#100]: https://github.com/koboldpress/black-flag/issues/100
[#101]: https://github.com/koboldpress/black-flag/issues/101
[#104]: https://github.com/koboldpress/black-flag/issues/104
[#105]: https://github.com/koboldpress/black-flag/issues/105
[#106]: https://github.com/koboldpress/black-flag/issues/106
[#107]: https://github.com/koboldpress/black-flag/issues/107
[#108]: https://github.com/koboldpress/black-flag/issues/108
[#109]: https://github.com/koboldpress/black-flag/issues/109
[#110]: https://github.com/koboldpress/black-flag/issues/110
[#111]: https://github.com/koboldpress/black-flag/issues/111
[#112]: https://github.com/koboldpress/black-flag/issues/112
[#113]: https://github.com/koboldpress/black-flag/issues/113
[#115]: https://github.com/koboldpress/black-flag/issues/115
[#116]: https://github.com/koboldpress/black-flag/issues/116
[#117]: https://github.com/koboldpress/black-flag/issues/117
[#118]: https://github.com/koboldpress/black-flag/issues/118
[#121]: https://github.com/koboldpress/black-flag/issues/121
[#122]: https://github.com/koboldpress/black-flag/issues/122
[#123]: https://github.com/koboldpress/black-flag/issues/123
[#124]: https://github.com/koboldpress/black-flag/issues/124
[#125]: https://github.com/koboldpress/black-flag/issues/125
[#126]: https://github.com/koboldpress/black-flag/issues/126
[#127]: https://github.com/koboldpress/black-flag/issues/127
[#128]: https://github.com/koboldpress/black-flag/issues/128
[#129]: https://github.com/koboldpress/black-flag/issues/129
[#130]: https://github.com/koboldpress/black-flag/issues/130
[#133]: https://github.com/koboldpress/black-flag/issues/133
[#137]: https://github.com/koboldpress/black-flag/issues/137
[#139]: https://github.com/koboldpress/black-flag/issues/139
[#140]: https://github.com/koboldpress/black-flag/issues/140
[#141]: https://github.com/koboldpress/black-flag/issues/141
[#142]: https://github.com/koboldpress/black-flag/issues/142
[#143]: https://github.com/koboldpress/black-flag/issues/143
[#144]: https://github.com/koboldpress/black-flag/issues/144
[#145]: https://github.com/koboldpress/black-flag/issues/145
[#146]: https://github.com/koboldpress/black-flag/issues/146
[#148]: https://github.com/koboldpress/black-flag/issues/148
[#149]: https://github.com/koboldpress/black-flag/issues/149
[#150]: https://github.com/koboldpress/black-flag/issues/150
[#151]: https://github.com/koboldpress/black-flag/issues/151
[#152]: https://github.com/koboldpress/black-flag/issues/152
[#153]: https://github.com/koboldpress/black-flag/issues/153
[#154]: https://github.com/koboldpress/black-flag/issues/154
[#156]: https://github.com/koboldpress/black-flag/issues/156
[#157]: https://github.com/koboldpress/black-flag/issues/157
[#158]: https://github.com/koboldpress/black-flag/issues/158
[#160]: https://github.com/koboldpress/black-flag/issues/160
[#161]: https://github.com/koboldpress/black-flag/issues/161
[#162]: https://github.com/koboldpress/black-flag/issues/162
[#163]: https://github.com/koboldpress/black-flag/issues/163
[#165]: https://github.com/koboldpress/black-flag/issues/165
[#166]: https://github.com/koboldpress/black-flag/issues/166
[#167]: https://github.com/koboldpress/black-flag/issues/167
[#168]: https://github.com/koboldpress/black-flag/issues/168
[#169]: https://github.com/koboldpress/black-flag/issues/169
[#170]: https://github.com/koboldpress/black-flag/issues/170
[#171]: https://github.com/koboldpress/black-flag/issues/171
[#172]: https://github.com/koboldpress/black-flag/issues/172
[#173]: https://github.com/koboldpress/black-flag/issues/173
[#174]: https://github.com/koboldpress/black-flag/issues/174
[#175]: https://github.com/koboldpress/black-flag/issues/175
[#176]: https://github.com/koboldpress/black-flag/issues/176
[#177]: https://github.com/koboldpress/black-flag/issues/177
[#178]: https://github.com/koboldpress/black-flag/issues/178
[#179]: https://github.com/koboldpress/black-flag/issues/179
[#180]: https://github.com/koboldpress/black-flag/issues/180
[#182]: https://github.com/koboldpress/black-flag/issues/182
[#185]: https://github.com/koboldpress/black-flag/issues/185
[#187]: https://github.com/koboldpress/black-flag/issues/187
[#188]: https://github.com/koboldpress/black-flag/issues/188
[#189]: https://github.com/koboldpress/black-flag/issues/189
[#190]: https://github.com/koboldpress/black-flag/issues/190
[#191]: https://github.com/koboldpress/black-flag/issues/191
[#192]: https://github.com/koboldpress/black-flag/issues/192
[#193]: https://github.com/koboldpress/black-flag/issues/193
[#194]: https://github.com/koboldpress/black-flag/issues/194
[#195]: https://github.com/koboldpress/black-flag/issues/195
[#196]: https://github.com/koboldpress/black-flag/issues/196
[#197]: https://github.com/koboldpress/black-flag/issues/197
[#198]: https://github.com/koboldpress/black-flag/issues/198
[#199]: https://github.com/koboldpress/black-flag/issues/199
[#200]: https://github.com/koboldpress/black-flag/issues/200
[#201]: https://github.com/koboldpress/black-flag/issues/201
[#202]: https://github.com/koboldpress/black-flag/issues/202
[#203]: https://github.com/koboldpress/black-flag/issues/203
[#204]: https://github.com/koboldpress/black-flag/issues/204
[#206]: https://github.com/koboldpress/black-flag/issues/206
[#207]: https://github.com/koboldpress/black-flag/issues/207
[#208]: https://github.com/koboldpress/black-flag/issues/208
[#209]: https://github.com/koboldpress/black-flag/issues/209
[#210]: https://github.com/koboldpress/black-flag/issues/210
[#211]: https://github.com/koboldpress/black-flag/issues/211
[#212]: https://github.com/koboldpress/black-flag/issues/212
[#213]: https://github.com/koboldpress/black-flag/issues/213
[#214]: https://github.com/koboldpress/black-flag/issues/214
[#215]: https://github.com/koboldpress/black-flag/issues/215
[#216]: https://github.com/koboldpress/black-flag/issues/216
[#217]: https://github.com/koboldpress/black-flag/issues/217
[#218]: https://github.com/koboldpress/black-flag/issues/218
[#219]: https://github.com/koboldpress/black-flag/issues/219
[#220]: https://github.com/koboldpress/black-flag/issues/220
[#221]: https://github.com/koboldpress/black-flag/issues/221
[#222]: https://github.com/koboldpress/black-flag/issues/222
[#224]: https://github.com/koboldpress/black-flag/issues/224
[#225]: https://github.com/koboldpress/black-flag/issues/225
[#226]: https://github.com/koboldpress/black-flag/issues/226
[#227]: https://github.com/koboldpress/black-flag/issues/227
[#228]: https://github.com/koboldpress/black-flag/issues/228
[#229]: https://github.com/koboldpress/black-flag/issues/229
[#230]: https://github.com/koboldpress/black-flag/issues/230
[#233]: https://github.com/koboldpress/black-flag/issues/233
[#235]: https://github.com/koboldpress/black-flag/issues/235
[#236]: https://github.com/koboldpress/black-flag/issues/236
[#237]: https://github.com/koboldpress/black-flag/issues/237
[#238]: https://github.com/koboldpress/black-flag/issues/238
[#239]: https://github.com/koboldpress/black-flag/issues/239
[#240]: https://github.com/koboldpress/black-flag/issues/240
[#241]: https://github.com/koboldpress/black-flag/issues/241
[#242]: https://github.com/koboldpress/black-flag/issues/242
[#243]: https://github.com/koboldpress/black-flag/issues/243
[#244]: https://github.com/koboldpress/black-flag/issues/244
[#245]: https://github.com/koboldpress/black-flag/issues/245
[#246]: https://github.com/koboldpress/black-flag/issues/246
[#247]: https://github.com/koboldpress/black-flag/issues/247
[#248]: https://github.com/koboldpress/black-flag/issues/248
[#249]: https://github.com/koboldpress/black-flag/issues/249
[#250]: https://github.com/koboldpress/black-flag/issues/250
[#251]: https://github.com/koboldpress/black-flag/issues/251
[#253]: https://github.com/koboldpress/black-flag/issues/253
[#254]: https://github.com/koboldpress/black-flag/issues/254
[#255]: https://github.com/koboldpress/black-flag/issues/255
[#256]: https://github.com/koboldpress/black-flag/issues/256
[#257]: https://github.com/koboldpress/black-flag/issues/257
[#258]: https://github.com/koboldpress/black-flag/issues/258
[#259]: https://github.com/koboldpress/black-flag/issues/259
[#260]: https://github.com/koboldpress/black-flag/issues/260
[#261]: https://github.com/koboldpress/black-flag/issues/261
[#262]: https://github.com/koboldpress/black-flag/issues/262
[#263]: https://github.com/koboldpress/black-flag/issues/263
[#264]: https://github.com/koboldpress/black-flag/issues/264
[#265]: https://github.com/koboldpress/black-flag/issues/265
[#266]: https://github.com/koboldpress/black-flag/issues/266
[#267]: https://github.com/koboldpress/black-flag/issues/267
[#268]: https://github.com/koboldpress/black-flag/issues/268
[#270]: https://github.com/koboldpress/black-flag/issues/270
[#271]: https://github.com/koboldpress/black-flag/issues/271
[#272]: https://github.com/koboldpress/black-flag/issues/272
[#273]: https://github.com/koboldpress/black-flag/issues/273
[#274]: https://github.com/koboldpress/black-flag/issues/274
[#275]: https://github.com/koboldpress/black-flag/issues/275
[#276]: https://github.com/koboldpress/black-flag/issues/276
[#280]: https://github.com/koboldpress/black-flag/issues/280
[#281]: https://github.com/koboldpress/black-flag/issues/281
[#282]: https://github.com/koboldpress/black-flag/issues/282
[#283]: https://github.com/koboldpress/black-flag/issues/283
[#284]: https://github.com/koboldpress/black-flag/issues/284
[#285]: https://github.com/koboldpress/black-flag/issues/285
[#286]: https://github.com/koboldpress/black-flag/issues/286
[#287]: https://github.com/koboldpress/black-flag/issues/287
[#288]: https://github.com/koboldpress/black-flag/issues/288
[#289]: https://github.com/koboldpress/black-flag/issues/289
[#290]: https://github.com/koboldpress/black-flag/issues/290
[#291]: https://github.com/koboldpress/black-flag/issues/291
[#293]: https://github.com/koboldpress/black-flag/issues/293
[#294]: https://github.com/koboldpress/black-flag/issues/294
[#295]: https://github.com/koboldpress/black-flag/issues/295
[#296]: https://github.com/koboldpress/black-flag/issues/296
[#297]: https://github.com/koboldpress/black-flag/issues/297
[#298]: https://github.com/koboldpress/black-flag/issues/298
[#299]: https://github.com/koboldpress/black-flag/issues/299
[#300]: https://github.com/koboldpress/black-flag/issues/300
[#301]: https://github.com/koboldpress/black-flag/issues/301
[#302]: https://github.com/koboldpress/black-flag/issues/302
[#303]: https://github.com/koboldpress/black-flag/issues/303
[#305]: https://github.com/koboldpress/black-flag/issues/305
[#306]: https://github.com/koboldpress/black-flag/issues/306
[#308]: https://github.com/koboldpress/black-flag/issues/308
[#309]: https://github.com/koboldpress/black-flag/issues/309
[#310]: https://github.com/koboldpress/black-flag/issues/310
[#311]: https://github.com/koboldpress/black-flag/issues/311
[#312]: https://github.com/koboldpress/black-flag/issues/312
[#314]: https://github.com/koboldpress/black-flag/issues/314
[#315]: https://github.com/koboldpress/black-flag/issues/315
[#316]: https://github.com/koboldpress/black-flag/issues/316
[#317]: https://github.com/koboldpress/black-flag/issues/317
[#318]: https://github.com/koboldpress/black-flag/issues/318
[#319]: https://github.com/koboldpress/black-flag/issues/319
[#320]: https://github.com/koboldpress/black-flag/issues/320
[#321]: https://github.com/koboldpress/black-flag/issues/321
[#323]: https://github.com/koboldpress/black-flag/issues/323
[#324]: https://github.com/koboldpress/black-flag/issues/324
[#325]: https://github.com/koboldpress/black-flag/issues/325
[#326]: https://github.com/koboldpress/black-flag/issues/326
[#327]: https://github.com/koboldpress/black-flag/issues/327
[#328]: https://github.com/koboldpress/black-flag/issues/328
[#329]: https://github.com/koboldpress/black-flag/issues/329
[#331]: https://github.com/koboldpress/black-flag/issues/331
[#332]: https://github.com/koboldpress/black-flag/issues/332
[#333]: https://github.com/koboldpress/black-flag/issues/333
[#334]: https://github.com/koboldpress/black-flag/issues/334
[#335]: https://github.com/koboldpress/black-flag/issues/335
[#336]: https://github.com/koboldpress/black-flag/issues/336
[#337]: https://github.com/koboldpress/black-flag/issues/337
[#338]: https://github.com/koboldpress/black-flag/issues/338
[#339]: https://github.com/koboldpress/black-flag/issues/339
[#340]: https://github.com/koboldpress/black-flag/issues/340
[#341]: https://github.com/koboldpress/black-flag/issues/341
[#342]: https://github.com/koboldpress/black-flag/issues/342
[#343]: https://github.com/koboldpress/black-flag/issues/343
[#344]: https://github.com/koboldpress/black-flag/issues/344
[#345]: https://github.com/koboldpress/black-flag/issues/345
[#346]: https://github.com/koboldpress/black-flag/issues/346
[#347]: https://github.com/koboldpress/black-flag/issues/347
[#348]: https://github.com/koboldpress/black-flag/issues/348
[#350]: https://github.com/koboldpress/black-flag/issues/350
[#352]: https://github.com/koboldpress/black-flag/issues/352
[#353]: https://github.com/koboldpress/black-flag/issues/353
[#355]: https://github.com/koboldpress/black-flag/issues/355
[#356]: https://github.com/koboldpress/black-flag/issues/356
[#357]: https://github.com/koboldpress/black-flag/issues/357
[#359]: https://github.com/koboldpress/black-flag/issues/359
[#360]: https://github.com/koboldpress/black-flag/issues/360
[#361]: https://github.com/koboldpress/black-flag/issues/361
[#363]: https://github.com/koboldpress/black-flag/issues/363
[#364]: https://github.com/koboldpress/black-flag/issues/364
[#368]: https://github.com/koboldpress/black-flag/issues/368
[#369]: https://github.com/koboldpress/black-flag/issues/369
[#370]: https://github.com/koboldpress/black-flag/issues/370
[#371]: https://github.com/koboldpress/black-flag/issues/371
[#372]: https://github.com/koboldpress/black-flag/issues/372
[#373]: https://github.com/koboldpress/black-flag/issues/373
[#374]: https://github.com/koboldpress/black-flag/issues/374
[#375]: https://github.com/koboldpress/black-flag/issues/375
[#376]: https://github.com/koboldpress/black-flag/issues/376
[#377]: https://github.com/koboldpress/black-flag/issues/377
[#378]: https://github.com/koboldpress/black-flag/issues/378
[#380]: https://github.com/koboldpress/black-flag/issues/381
[#381]: https://github.com/koboldpress/black-flag/issues/381
[#382]: https://github.com/koboldpress/black-flag/issues/382
[#383]: https://github.com/koboldpress/black-flag/issues/383
[#384]: https://github.com/koboldpress/black-flag/issues/384
[#385]: https://github.com/koboldpress/black-flag/issues/385
[#386]: https://github.com/koboldpress/black-flag/issues/386
[#387]: https://github.com/koboldpress/black-flag/issues/387
[#388]: https://github.com/koboldpress/black-flag/issues/388
[#389]: https://github.com/koboldpress/black-flag/issues/389
[#390]: https://github.com/koboldpress/black-flag/issues/390
[#391]: https://github.com/koboldpress/black-flag/issues/391
[#392]: https://github.com/koboldpress/black-flag/issues/392
[#393]: https://github.com/koboldpress/black-flag/issues/393
[#394]: https://github.com/koboldpress/black-flag/issues/394
[#395]: https://github.com/koboldpress/black-flag/issues/395
[#396]: https://github.com/koboldpress/black-flag/issues/396
[#397]: https://github.com/koboldpress/black-flag/issues/397
[#398]: https://github.com/koboldpress/black-flag/issues/398
[#399]: https://github.com/koboldpress/black-flag/issues/399
[#400]: https://github.com/koboldpress/black-flag/issues/400
[#401]: https://github.com/koboldpress/black-flag/issues/401
[#402]: https://github.com/koboldpress/black-flag/issues/402
[#403]: https://github.com/koboldpress/black-flag/issues/403
[#404]: https://github.com/koboldpress/black-flag/issues/404
[#405]: https://github.com/koboldpress/black-flag/issues/405
[#406]: https://github.com/koboldpress/black-flag/issues/406
[#407]: https://github.com/koboldpress/black-flag/issues/407
[#408]: https://github.com/koboldpress/black-flag/issues/408
[#410]: https://github.com/koboldpress/black-flag/issues/410
[#411]: https://github.com/koboldpress/black-flag/issues/411
[#412]: https://github.com/koboldpress/black-flag/issues/412
[#413]: https://github.com/koboldpress/black-flag/issues/413
[#414]: https://github.com/koboldpress/black-flag/issues/414
[#415]: https://github.com/koboldpress/black-flag/issues/415
[#416]: https://github.com/koboldpress/black-flag/issues/416
[#417]: https://github.com/koboldpress/black-flag/issues/417
[#418]: https://github.com/koboldpress/black-flag/issues/418
[#419]: https://github.com/koboldpress/black-flag/issues/419
[#420]: https://github.com/koboldpress/black-flag/issues/420
[#421]: https://github.com/koboldpress/black-flag/issues/421
[#422]: https://github.com/koboldpress/black-flag/issues/422
[#423]: https://github.com/koboldpress/black-flag/issues/423
[#424]: https://github.com/koboldpress/black-flag/issues/424
[#425]: https://github.com/koboldpress/black-flag/issues/425
[#426]: https://github.com/koboldpress/black-flag/issues/426
[#427]: https://github.com/koboldpress/black-flag/issues/427
[#428]: https://github.com/koboldpress/black-flag/issues/428
[#429]: https://github.com/koboldpress/black-flag/issues/429
[#430]: https://github.com/koboldpress/black-flag/issues/430
[#432]: https://github.com/koboldpress/black-flag/issues/432
[#433]: https://github.com/koboldpress/black-flag/issues/433
[#434]: https://github.com/koboldpress/black-flag/issues/434
[#435]: https://github.com/koboldpress/black-flag/issues/435
[#436]: https://github.com/koboldpress/black-flag/issues/436
[#437]: https://github.com/koboldpress/black-flag/issues/437
[#438]: https://github.com/koboldpress/black-flag/issues/438
[#439]: https://github.com/koboldpress/black-flag/issues/439
[#440]: https://github.com/koboldpress/black-flag/issues/440
[#441]: https://github.com/koboldpress/black-flag/issues/441
[#442]: https://github.com/koboldpress/black-flag/issues/442
[#444]: https://github.com/koboldpress/black-flag/issues/444
[#445]: https://github.com/koboldpress/black-flag/issues/445
[#446]: https://github.com/koboldpress/black-flag/issues/446
[#450]: https://github.com/koboldpress/black-flag/issues/450
[#451]: https://github.com/koboldpress/black-flag/issues/451
[#452]: https://github.com/koboldpress/black-flag/issues/452
[#453]: https://github.com/koboldpress/black-flag/issues/453
[#454]: https://github.com/koboldpress/black-flag/issues/454
[#455]: https://github.com/koboldpress/black-flag/issues/455
[#456]: https://github.com/koboldpress/black-flag/issues/456
[#458]: https://github.com/koboldpress/black-flag/issues/458
[#459]: https://github.com/koboldpress/black-flag/issues/459
[#460]: https://github.com/koboldpress/black-flag/issues/460
[#462]: https://github.com/koboldpress/black-flag/issues/462
[#463]: https://github.com/koboldpress/black-flag/issues/463
[#464]: https://github.com/koboldpress/black-flag/issues/464
[#465]: https://github.com/koboldpress/black-flag/issues/465
[#466]: https://github.com/koboldpress/black-flag/issues/466
[#467]: https://github.com/koboldpress/black-flag/issues/467
[#468]: https://github.com/koboldpress/black-flag/issues/468
[#469]: https://github.com/koboldpress/black-flag/issues/469
[#470]: https://github.com/koboldpress/black-flag/issues/470
[#471]: https://github.com/koboldpress/black-flag/issues/471
[#472]: https://github.com/koboldpress/black-flag/issues/472
[#474]: https://github.com/koboldpress/black-flag/issues/474
[#475]: https://github.com/koboldpress/black-flag/issues/475
[#476]: https://github.com/koboldpress/black-flag/issues/476
[#478]: https://github.com/koboldpress/black-flag/issues/478
[#479]: https://github.com/koboldpress/black-flag/issues/479
[#481]: https://github.com/koboldpress/black-flag/issues/481
[#482]: https://github.com/koboldpress/black-flag/issues/482
[#486]: https://github.com/koboldpress/black-flag/issues/486
[#490]: https://github.com/koboldpress/black-flag/issues/490
[#493]: https://github.com/koboldpress/black-flag/issues/493
[#495]: https://github.com/koboldpress/black-flag/issues/495
[#496]: https://github.com/koboldpress/black-flag/issues/496
[#497]: https://github.com/koboldpress/black-flag/issues/497
[#498]: https://github.com/koboldpress/black-flag/issues/498
[#499]: https://github.com/koboldpress/black-flag/issues/499
[#500]: https://github.com/koboldpress/black-flag/issues/500
[#501]: https://github.com/koboldpress/black-flag/issues/501
[#503]: https://github.com/koboldpress/black-flag/issues/503
[#505]: https://github.com/koboldpress/black-flag/issues/505
[#506]: https://github.com/koboldpress/black-flag/issues/506
[#507]: https://github.com/koboldpress/black-flag/issues/507
[#508]: https://github.com/koboldpress/black-flag/issues/508
[#509]: https://github.com/koboldpress/black-flag/issues/509
[#511]: https://github.com/koboldpress/black-flag/issues/511
[#513]: https://github.com/koboldpress/black-flag/issues/513
[#514]: https://github.com/koboldpress/black-flag/issues/514
[#515]: https://github.com/koboldpress/black-flag/issues/515
[#517]: https://github.com/koboldpress/black-flag/issues/517
[#518]: https://github.com/koboldpress/black-flag/issues/518
[#521]: https://github.com/koboldpress/black-flag/issues/521
[#522]: https://github.com/koboldpress/black-flag/issues/522
[#523]: https://github.com/koboldpress/black-flag/issues/523
[#524]: https://github.com/koboldpress/black-flag/issues/524
[#525]: https://github.com/koboldpress/black-flag/issues/525
[#526]: https://github.com/koboldpress/black-flag/issues/526
[#527]: https://github.com/koboldpress/black-flag/issues/527
[#528]: https://github.com/koboldpress/black-flag/issues/528
[#529]: https://github.com/koboldpress/black-flag/issues/529
[#530]: https://github.com/koboldpress/black-flag/issues/530
[#531]: https://github.com/koboldpress/black-flag/issues/531
[#534]: https://github.com/koboldpress/black-flag/issues/534
[#535]: https://github.com/koboldpress/black-flag/issues/535
[#536]: https://github.com/koboldpress/black-flag/issues/536
[#537]: https://github.com/koboldpress/black-flag/issues/537
[#539]: https://github.com/koboldpress/black-flag/issues/539
[#541]: https://github.com/koboldpress/black-flag/issues/541
[#542]: https://github.com/koboldpress/black-flag/issues/542
[#543]: https://github.com/koboldpress/black-flag/issues/543
[#544]: https://github.com/koboldpress/black-flag/issues/544
[#546]: https://github.com/koboldpress/black-flag/issues/546
[#547]: https://github.com/koboldpress/black-flag/issues/547
[#548]: https://github.com/koboldpress/black-flag/issues/548
[#549]: https://github.com/koboldpress/black-flag/issues/549
[#550]: https://github.com/koboldpress/black-flag/issues/550
[#553]: https://github.com/koboldpress/black-flag/issues/553
[#554]: https://github.com/koboldpress/black-flag/issues/554
[#555]: https://github.com/koboldpress/black-flag/issues/555
[#556]: https://github.com/koboldpress/black-flag/issues/556
[#557]: https://github.com/koboldpress/black-flag/issues/557
[#558]: https://github.com/koboldpress/black-flag/issues/558
[#559]: https://github.com/koboldpress/black-flag/issues/559
[#560]: https://github.com/koboldpress/black-flag/issues/560
[#561]: https://github.com/koboldpress/black-flag/issues/561
[#562]: https://github.com/koboldpress/black-flag/issues/562
[#566]: https://github.com/koboldpress/black-flag/issues/566
[#567]: https://github.com/koboldpress/black-flag/issues/567
[#568]: https://github.com/koboldpress/black-flag/issues/568
[#569]: https://github.com/koboldpress/black-flag/issues/569
[#570]: https://github.com/koboldpress/black-flag/issues/570
[#571]: https://github.com/koboldpress/black-flag/issues/571
[#572]: https://github.com/koboldpress/black-flag/issues/572
[#573]: https://github.com/koboldpress/black-flag/issues/573
[#574]: https://github.com/koboldpress/black-flag/issues/574
[#575]: https://github.com/koboldpress/black-flag/issues/575
[#577]: https://github.com/koboldpress/black-flag/issues/577
[#579]: https://github.com/koboldpress/black-flag/issues/579
[#580]: https://github.com/koboldpress/black-flag/issues/580
[#581]: https://github.com/koboldpress/black-flag/issues/581
[#582]: https://github.com/koboldpress/black-flag/issues/582
[#583]: https://github.com/koboldpress/black-flag/issues/583
[#584]: https://github.com/koboldpress/black-flag/issues/584
[#585]: https://github.com/koboldpress/black-flag/issues/585
[#586]: https://github.com/koboldpress/black-flag/issues/586
[#587]: https://github.com/koboldpress/black-flag/issues/587
[#588]: https://github.com/koboldpress/black-flag/issues/588
[#589]: https://github.com/koboldpress/black-flag/issues/589
[#591]: https://github.com/koboldpress/black-flag/issues/591
[#592]: https://github.com/koboldpress/black-flag/issues/592
[#594]: https://github.com/koboldpress/black-flag/issues/594
[#595]: https://github.com/koboldpress/black-flag/issues/595
[#596]: https://github.com/koboldpress/black-flag/issues/596
[#598]: https://github.com/koboldpress/black-flag/issues/598
[#599]: https://github.com/koboldpress/black-flag/issues/599
[#600]: https://github.com/koboldpress/black-flag/issues/600
[#602]: https://github.com/koboldpress/black-flag/issues/602
[#603]: https://github.com/koboldpress/black-flag/issues/603
[#606]: https://github.com/koboldpress/black-flag/issues/606
[#607]: https://github.com/koboldpress/black-flag/issues/607
[#610]: https://github.com/koboldpress/black-flag/issues/610
[#612]: https://github.com/koboldpress/black-flag/issues/612
[#613]: https://github.com/koboldpress/black-flag/issues/613
[#614]: https://github.com/koboldpress/black-flag/issues/614
[#615]: https://github.com/koboldpress/black-flag/issues/615
[#616]: https://github.com/koboldpress/black-flag/issues/616
[#617]: https://github.com/koboldpress/black-flag/issues/617
[#618]: https://github.com/koboldpress/black-flag/issues/618
[#620]: https://github.com/koboldpress/black-flag/issues/620
[#622]: https://github.com/koboldpress/black-flag/issues/622
[#623]: https://github.com/koboldpress/black-flag/issues/623
[#624]: https://github.com/koboldpress/black-flag/issues/624
[#626]: https://github.com/koboldpress/black-flag/issues/626
[#627]: https://github.com/koboldpress/black-flag/issues/627
[#628]: https://github.com/koboldpress/black-flag/issues/628
[#629]: https://github.com/koboldpress/black-flag/issues/629
[#630]: https://github.com/koboldpress/black-flag/issues/630
[#631]: https://github.com/koboldpress/black-flag/issues/631
[#632]: https://github.com/koboldpress/black-flag/issues/632
[#634]: https://github.com/koboldpress/black-flag/issues/634
[#635]: https://github.com/koboldpress/black-flag/issues/635
[#636]: https://github.com/koboldpress/black-flag/issues/636
[#637]: https://github.com/koboldpress/black-flag/issues/637
[#638]: https://github.com/koboldpress/black-flag/issues/638
[#639]: https://github.com/koboldpress/black-flag/issues/639
[#642]: https://github.com/koboldpress/black-flag/issues/642
[#644]: https://github.com/koboldpress/black-flag/issues/644
[#645]: https://github.com/koboldpress/black-flag/issues/645
[#647]: https://github.com/koboldpress/black-flag/issues/647
[#648]: https://github.com/koboldpress/black-flag/issues/648
[#649]: https://github.com/koboldpress/black-flag/issues/649
[#650]: https://github.com/koboldpress/black-flag/issues/650
[#651]: https://github.com/koboldpress/black-flag/issues/651
[#652]: https://github.com/koboldpress/black-flag/issues/652
[#653]: https://github.com/koboldpress/black-flag/issues/653
[#654]: https://github.com/koboldpress/black-flag/issues/654
[#655]: https://github.com/koboldpress/black-flag/issues/655
[#656]: https://github.com/koboldpress/black-flag/issues/656
[#658]: https://github.com/koboldpress/black-flag/issues/658
[#659]: https://github.com/koboldpress/black-flag/issues/659
[#660]: https://github.com/koboldpress/black-flag/issues/660
[#661]: https://github.com/koboldpress/black-flag/issues/661
[#662]: https://github.com/koboldpress/black-flag/issues/662
[#663]: https://github.com/koboldpress/black-flag/issues/663
[#664]: https://github.com/koboldpress/black-flag/issues/664
[#665]: https://github.com/koboldpress/black-flag/issues/665
[#666]: https://github.com/koboldpress/black-flag/issues/666
[#667]: https://github.com/koboldpress/black-flag/issues/667
[#668]: https://github.com/koboldpress/black-flag/issues/668
[#669]: https://github.com/koboldpress/black-flag/issues/669
[#670]: https://github.com/koboldpress/black-flag/issues/670
[#671]: https://github.com/koboldpress/black-flag/issues/671
[#672]: https://github.com/koboldpress/black-flag/issues/672
[#675]: https://github.com/koboldpress/black-flag/issues/675
[#676]: https://github.com/koboldpress/black-flag/issues/676
[#677]: https://github.com/koboldpress/black-flag/issues/677
[#678]: https://github.com/koboldpress/black-flag/issues/678
[#679]: https://github.com/koboldpress/black-flag/issues/679
[#680]: https://github.com/koboldpress/black-flag/issues/680
[#681]: https://github.com/koboldpress/black-flag/issues/681
[#682]: https://github.com/koboldpress/black-flag/issues/682
[#683]: https://github.com/koboldpress/black-flag/issues/683
[#686]: https://github.com/koboldpress/black-flag/issues/686
[#688]: https://github.com/koboldpress/black-flag/issues/688
[#689]: https://github.com/koboldpress/black-flag/issues/689
[#690]: https://github.com/koboldpress/black-flag/issues/690
[#691]: https://github.com/koboldpress/black-flag/issues/691
[#692]: https://github.com/koboldpress/black-flag/issues/692
[#693]: https://github.com/koboldpress/black-flag/issues/693
[#694]: https://github.com/koboldpress/black-flag/issues/694
[#695]: https://github.com/koboldpress/black-flag/issues/695
[#696]: https://github.com/koboldpress/black-flag/issues/696
[#697]: https://github.com/koboldpress/black-flag/issues/697
[#698]: https://github.com/koboldpress/black-flag/issues/698
[#699]: https://github.com/koboldpress/black-flag/issues/699
[#700]: https://github.com/koboldpress/black-flag/issues/700
[#701]: https://github.com/koboldpress/black-flag/issues/701
[#702]: https://github.com/koboldpress/black-flag/issues/702
[#703]: https://github.com/koboldpress/black-flag/issues/703
[#704]: https://github.com/koboldpress/black-flag/issues/704
[#705]: https://github.com/koboldpress/black-flag/issues/705
[#706]: https://github.com/koboldpress/black-flag/issues/706
[#707]: https://github.com/koboldpress/black-flag/issues/707
[#708]: https://github.com/koboldpress/black-flag/issues/708
[#709]: https://github.com/koboldpress/black-flag/issues/709
[#710]: https://github.com/koboldpress/black-flag/issues/710
[#711]: https://github.com/koboldpress/black-flag/issues/711
[#712]: https://github.com/koboldpress/black-flag/issues/712
[#714]: https://github.com/koboldpress/black-flag/issues/714
[#715]: https://github.com/koboldpress/black-flag/issues/715
[#716]: https://github.com/koboldpress/black-flag/issues/716
[#717]: https://github.com/koboldpress/black-flag/issues/717
[#718]: https://github.com/koboldpress/black-flag/issues/718
[#719]: https://github.com/koboldpress/black-flag/issues/719
[#720]: https://github.com/koboldpress/black-flag/issues/720
[#721]: https://github.com/koboldpress/black-flag/issues/721
[#722]: https://github.com/koboldpress/black-flag/issues/722
[#723]: https://github.com/koboldpress/black-flag/issues/723
[#725]: https://github.com/koboldpress/black-flag/issues/725
[#727]: https://github.com/koboldpress/black-flag/issues/727
[#728]: https://github.com/koboldpress/black-flag/issues/728
[#729]: https://github.com/koboldpress/black-flag/issues/729
[#730]: https://github.com/koboldpress/black-flag/issues/730
[#731]: https://github.com/koboldpress/black-flag/issues/731
[#732]: https://github.com/koboldpress/black-flag/issues/732
[#733]: https://github.com/koboldpress/black-flag/issues/733
[#734]: https://github.com/koboldpress/black-flag/issues/734
[#735]: https://github.com/koboldpress/black-flag/issues/735
[#736]: https://github.com/koboldpress/black-flag/issues/736
[#737]: https://github.com/koboldpress/black-flag/issues/737
[#738]: https://github.com/koboldpress/black-flag/issues/738
[#739]: https://github.com/koboldpress/black-flag/issues/739
[#740]: https://github.com/koboldpress/black-flag/issues/740
[#742]: https://github.com/koboldpress/black-flag/issues/742
[#743]: https://github.com/koboldpress/black-flag/issues/743
[#744]: https://github.com/koboldpress/black-flag/issues/744
[#745]: https://github.com/koboldpress/black-flag/issues/745
[#746]: https://github.com/koboldpress/black-flag/issues/746
[#749]: https://github.com/koboldpress/black-flag/issues/749
[#750]: https://github.com/koboldpress/black-flag/issues/750
[#751]: https://github.com/koboldpress/black-flag/issues/751
[#752]: https://github.com/koboldpress/black-flag/issues/752
[#755]: https://github.com/koboldpress/black-flag/issues/755
[#756]: https://github.com/koboldpress/black-flag/issues/756
[#757]: https://github.com/koboldpress/black-flag/issues/757
[#760]: https://github.com/koboldpress/black-flag/issues/760
[#761]: https://github.com/koboldpress/black-flag/issues/761
[#762]: https://github.com/koboldpress/black-flag/issues/762
[#764]: https://github.com/koboldpress/black-flag/issues/764
[#765]: https://github.com/koboldpress/black-flag/issues/765
[#766]: https://github.com/koboldpress/black-flag/issues/766
[#767]: https://github.com/koboldpress/black-flag/issues/767
[#768]: https://github.com/koboldpress/black-flag/issues/768
[#769]: https://github.com/koboldpress/black-flag/issues/769
[#770]: https://github.com/koboldpress/black-flag/issues/770
[#771]: https://github.com/koboldpress/black-flag/issues/771
[#772]: https://github.com/koboldpress/black-flag/issues/772
[#773]: https://github.com/koboldpress/black-flag/issues/773
[#775]: https://github.com/koboldpress/black-flag/issues/775
[#776]: https://github.com/koboldpress/black-flag/issues/776
[#777]: https://github.com/koboldpress/black-flag/issues/777
[#778]: https://github.com/koboldpress/black-flag/issues/778
[#779]: https://github.com/koboldpress/black-flag/issues/779
[#780]: https://github.com/koboldpress/black-flag/issues/780
[#781]: https://github.com/koboldpress/black-flag/issues/781
[#782]: https://github.com/koboldpress/black-flag/issues/782
[#784]: https://github.com/koboldpress/black-flag/issues/784
[#785]: https://github.com/koboldpress/black-flag/issues/785
[#786]: https://github.com/koboldpress/black-flag/issues/786
[#787]: https://github.com/koboldpress/black-flag/issues/787
[#788]: https://github.com/koboldpress/black-flag/issues/788
[#789]: https://github.com/koboldpress/black-flag/issues/789
[#791]: https://github.com/koboldpress/black-flag/issues/791
[#792]: https://github.com/koboldpress/black-flag/issues/792
[#793]: https://github.com/koboldpress/black-flag/issues/793
[#794]: https://github.com/koboldpress/black-flag/issues/794
[#795]: https://github.com/koboldpress/black-flag/issues/795
[#796]: https://github.com/koboldpress/black-flag/issues/796
[#797]: https://github.com/koboldpress/black-flag/issues/797
[#798]: https://github.com/koboldpress/black-flag/issues/798
[#799]: https://github.com/koboldpress/black-flag/issues/799
[#800]: https://github.com/koboldpress/black-flag/issues/800
[#801]: https://github.com/koboldpress/black-flag/issues/801
[#802]: https://github.com/koboldpress/black-flag/issues/802
[#804]: https://github.com/koboldpress/black-flag/issues/804
[#806]: https://github.com/koboldpress/black-flag/issues/806
[#807]: https://github.com/koboldpress/black-flag/issues/807
[#808]: https://github.com/koboldpress/black-flag/issues/808
[#810]: https://github.com/koboldpress/black-flag/issues/810
[#811]: https://github.com/koboldpress/black-flag/issues/811
[#812]: https://github.com/koboldpress/black-flag/issues/812
[#813]: https://github.com/koboldpress/black-flag/issues/813
[#815]: https://github.com/koboldpress/black-flag/issues/815
[#821]: https://github.com/koboldpress/black-flag/issues/821
[#823]: https://github.com/koboldpress/black-flag/issues/823
[#824]: https://github.com/koboldpress/black-flag/issues/824
[#826]: https://github.com/koboldpress/black-flag/issues/826
[#827]: https://github.com/koboldpress/black-flag/issues/827
[#828]: https://github.com/koboldpress/black-flag/issues/828
[#829]: https://github.com/koboldpress/black-flag/issues/829
[#830]: https://github.com/koboldpress/black-flag/issues/830
[#831]: https://github.com/koboldpress/black-flag/issues/831
[#832]: https://github.com/koboldpress/black-flag/issues/832
[#833]: https://github.com/koboldpress/black-flag/issues/833
[#834]: https://github.com/koboldpress/black-flag/issues/834
[#836]: https://github.com/koboldpress/black-flag/issues/836
[#837]: https://github.com/koboldpress/black-flag/issues/837
[#838]: https://github.com/koboldpress/black-flag/issues/838
[#839]: https://github.com/koboldpress/black-flag/issues/839
[#840]: https://github.com/koboldpress/black-flag/issues/840
[#841]: https://github.com/koboldpress/black-flag/issues/841
[#843]: https://github.com/koboldpress/black-flag/issues/843
[#844]: https://github.com/koboldpress/black-flag/issues/844
[#845]: https://github.com/koboldpress/black-flag/issues/845
[#846]: https://github.com/koboldpress/black-flag/issues/846
[#847]: https://github.com/koboldpress/black-flag/issues/847
[#848]: https://github.com/koboldpress/black-flag/issues/848
[#849]: https://github.com/koboldpress/black-flag/issues/849
[#850]: https://github.com/koboldpress/black-flag/issues/850
[#851]: https://github.com/koboldpress/black-flag/issues/851
[#852]: https://github.com/koboldpress/black-flag/issues/852
[#853]: https://github.com/koboldpress/black-flag/issues/853
[#856]: https://github.com/koboldpress/black-flag/issues/856
[#857]: https://github.com/koboldpress/black-flag/issues/857
[#858]: https://github.com/koboldpress/black-flag/issues/858
[#859]: https://github.com/koboldpress/black-flag/issues/859
[#860]: https://github.com/koboldpress/black-flag/issues/860
[#861]: https://github.com/koboldpress/black-flag/issues/861
[#862]: https://github.com/koboldpress/black-flag/issues/862
[#867]: https://github.com/koboldpress/black-flag/issues/867
[#868]: https://github.com/koboldpress/black-flag/issues/868
[#870]: https://github.com/koboldpress/black-flag/issues/870
[#871]: https://github.com/koboldpress/black-flag/issues/871
[#872]: https://github.com/koboldpress/black-flag/issues/872
[#874]: https://github.com/koboldpress/black-flag/issues/874
[#875]: https://github.com/koboldpress/black-flag/issues/875
[#876]: https://github.com/koboldpress/black-flag/issues/876
[#877]: https://github.com/koboldpress/black-flag/issues/877
[#878]: https://github.com/koboldpress/black-flag/issues/878
[#880]: https://github.com/koboldpress/black-flag/issues/880
[#881]: https://github.com/koboldpress/black-flag/issues/881
[#882]: https://github.com/koboldpress/black-flag/issues/882
[#883]: https://github.com/koboldpress/black-flag/issues/883
[#884]: https://github.com/koboldpress/black-flag/issues/884
[#885]: https://github.com/koboldpress/black-flag/issues/885
[#886]: https://github.com/koboldpress/black-flag/issues/886
[#887]: https://github.com/koboldpress/black-flag/issues/887
[#888]: https://github.com/koboldpress/black-flag/issues/888
[#890]: https://github.com/koboldpress/black-flag/issues/890
[#891]: https://github.com/koboldpress/black-flag/issues/891
[#893]: https://github.com/koboldpress/black-flag/issues/893
[#894]: https://github.com/koboldpress/black-flag/issues/894
[#895]: https://github.com/koboldpress/black-flag/issues/895
[#896]: https://github.com/koboldpress/black-flag/issues/896
[#897]: https://github.com/koboldpress/black-flag/issues/897
[#898]: https://github.com/koboldpress/black-flag/issues/898
[#899]: https://github.com/koboldpress/black-flag/issues/899
[#900]: https://github.com/koboldpress/black-flag/issues/900
[#901]: https://github.com/koboldpress/black-flag/issues/901
[#902]: https://github.com/koboldpress/black-flag/issues/902
[#904]: https://github.com/koboldpress/black-flag/issues/904
[#906]: https://github.com/koboldpress/black-flag/issues/906
[#907]: https://github.com/koboldpress/black-flag/issues/907
[#909]: https://github.com/koboldpress/black-flag/issues/909
[#914]: https://github.com/koboldpress/black-flag/issues/914
[#917]: https://github.com/koboldpress/black-flag/issues/917
[#918]: https://github.com/koboldpress/black-flag/issues/918
[#924]: https://github.com/koboldpress/black-flag/issues/924
[#927]: https://github.com/koboldpress/black-flag/issues/927
[#928]: https://github.com/koboldpress/black-flag/issues/928
[#929]: https://github.com/koboldpress/black-flag/issues/929
[#930]: https://github.com/koboldpress/black-flag/issues/930
[#931]: https://github.com/koboldpress/black-flag/issues/931
[#932]: https://github.com/koboldpress/black-flag/issues/932
[#933]: https://github.com/koboldpress/black-flag/issues/933
[#936]: https://github.com/koboldpress/black-flag/issues/936
