---
layout: page
title: Dungeons & Ruins Changelog
permalink: /changelogs/dungeons-ruins
---

# Campaign Builder: Dungeons & Ruins

## 14.0.0

- Updated the manifest to Foundry VTT core v14 and Black Flag v3.0.079.

### Subclasses

#### Barbarian: Mycelial

- **Fungal Rebuke:** Changed the activation from an Action to a Reaction.
- **Fungal Rebuke:** Corrected the damage formula to scale with Barbarian level.
- **Empowered Spore Aura:** Removed a broken Active Effect reference from Necrotic Spores.
- **Empowered Spore Aura:** Updated the activity configuration for the Necrotic Spores healing option.
- **Spore Aura:** Updated Active Effects for Black Flag v3 and Foundry VTT v14 compatibility.
- **Spore Aura:** Corrected the descriptions of the Phrenic Spores effects.

#### Bard: Elegy

- **Power from the Grave:** Separated the Bonus Action activation from the additional necrotic damage roll.
- **Power from the Grave:** Added a one-minute Active Effect to track the feature's duration.
- **Power from the Grave:** Updated the damage activity to use a Free activation without consuming additional uses.
- **Power from the Grave:** Changed the damage activity's duration to Instantaneous.
- **Spiritual Protection:** Corrected Bardic Inspiration consumption so expended uses are deducted and recovered uses are restored.
- **Spiritual Protection:** Changed both resource-management activities to Free activations.
- **Spiritual Protection:** Disabled the unnecessary Target Prompt on the recovery activity.

#### Mechanist: Demolitionist

- **Disruptive Force:** Updated Drain and Glitch to use the correct saving throw and damage settings.
- **Disruptive Force:** Updated Active Effects for Foundry VTT v14 compatibility and corrected their descriptions.
- **Catastrophic Force:** Corrected the subclass association and Glitch attack configuration.
- **Catastrophic Force:** Fixed the duration roll to use `1d4 + 1` rounds.
- **Catastrophic Force:** Repaired legacy Active Effects that prevented changes from being saved.
- **Catastrophic Force:** Updated effect descriptions and corrected the Drain saving throw settings.
- **Greater Destruction:** Updated Demolish to include objects being worn or held.
- **Total Destruction:** Updated Demolish targeting to include objects being worn or held.

#### Mechanist Augment Effect

- **Unmake:** Added an activity to set or change the trigger, corrected the Explode range to 60 feet, and updated targeting to exclude worn or held items.

#### Ranger: Spelunker

- **Cave Crawler:** Updated Climb Speed and Swim Speed Active Effects for Foundry VTT v14 and Black Flag 3 compatibility, updated their durations and descriptions.
- **Subterranean Master:** Updated the Keensense Active Effect for Foundry VTT v14 and Black Flag 3 compatibility.

#### Wizard: Reclaimer

- **Habituated Arcana:** Updated Arcana proficiency to grant Expertise to characters already proficient in the skill.
- **Magic Item Paroxysm:** Added an Action activity for detonating magic items.
- **Magic Item Paroxysm:** Corrected the saving throw settings and updated the explosion description.

### Heritages

#### Ashlayer

- **Arcane Wisdom:** Added an Active Effect reminder for bonuses to checks involving magical artifacts.
- **Careful Exploration:** Added an Active Effect reminder for advantage on checks involving traps, doors, and hazards in ruins.

#### Pathways Clan

- **Subterranean Navigation:** Added an Active Effect reminder for Perception checks in dim light while underground.
- **Underground Speed:** Updated the Active Effect for Foundry v14, corrected the burrowing speed formula, and added immunity to difficult terrain while underground.

#### Smoke

- **No Secrets Between Us:** Added an Active Effect reminder for advantage on Insight checks to detect lies and the follow-up check to uncover hidden information.
- **Silver-Tongued:** Updated the advancement hint and added an Active Effect reminder for the Deception bonus during transactions.

#### Unmoored

- **Always Learning:** Added an Active Effect reminder for the proficiency bonus gained from training in a skill during a long rest.

### Talents

#### Magic

- **Parting Shot:** Added separate Bonus Action activities for both cantrip-casting options, each with its own once-per-long-rest use.
- **Source Resistance:** Removed incorrect usage limits and Reaction requirements from both activities. Added the Spellcasting Class Feature prerequisite.

#### Martial

- **Side By Side:** Updated the temporary hit point activity with the correct activation condition.
- **Stalwart:** Added Plant Your Feet, corrected activity activation types and conditions, and organized the activities in rules order.

#### Technical

- **Breaker:** Added Inspect for Weaknesses, corrected the damage reroll activity, and updated the Active Effect's attack and damage modifiers.
- **Eidetic Memory:** Added a once-per-short-rest activity to track failed knowledge check rerolls.
- **Skeptic:** Named the illusion and mimicry activity and corrected the charm-save reroll condition.
- **Strong Stomach:** Migrated the Active Effect to Foundry v14's Base type.
- **Tunneler:** Migrated the Burrowing Speed Active Effect to Foundry v14's Base type.

### Spells

#### 1st-Circle

- **Aura of Alertness:** Named the spell's Utility activity.
- **Sure-Footed:** Corrected the Active Effect duration to 1 hour and added higher-circle targeting support, allowing one additional creature per spell circle above 1st.

#### 2nd-Circle

- **Alter Aura:** Migrated all Active Effects to Foundry v14, corrected the Aberration creature type, standardized effect durations to 1 hour, and reset elapsed-time tracking.

#### 3rd-Circle

- **Ooze Embodiment:** Migrated the Ooze Form Active Effect to Foundry v14, corrected walking and climbing speed modifiers, preserved condition resistances and immunities, and reset effect duration and elapsed-time tracking.

#### 4th-Circle

- **Become Shadow:** Migrated Active Effects to Foundry v14, corrected damage immunity attributes, reset effect duration and elapsed time, and updated the Foundry Note.
- **Elemental Perfusion:** Migrated all four Active Effects to Foundry v14, corrected movement and damage modifiers, and standardized effect durations.
- **Hungry Earth:** Corrected the Restrained Active Effect, including its condition, icon, and duration.
- **Rising Tide:** Corrected targeting to support all creatures within the affected area.
- **Scouring Wind:** Corrected target count and line width to match the spell's area of effect.
- **Wall of Darkness:** Corrected target selection and set the Blinded Active Effect duration to 1 minute.

#### 5th-Circle

- **Angelic Aspect:** Migrated the Active Effect to Foundry v14, corrected the melee damage modifier, and reset effect duration and elapsed time.
- **Devilish Aspect:** Migrated the Active Effect to Foundry v14, corrected the melee damage modifier, and reset effect duration and elapsed time.
- **Wall of Spirits:** Updated the Frightened Active Effect duration and corrected spell and effect descriptions.

#### 6th-Circle

- **Raining Fire:** Corrected targeting to affect all creatures within the spell's area.

---

### 13.0.1
- Restored organization for roll tables in the compendium
- Added “Creating a Hex Map” application and Hex Flower scenes

---

### 13.0.0
- Initial Release
