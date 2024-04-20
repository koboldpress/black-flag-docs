---
layout: page
title: Roll Formulas
permalink: /documentation/roll-formulas
---

![Up to date as of 0.9.022](https://img.shields.io/static/v1?label=black-flag&message=0.9.022&color=informational)

## Actor Properties

### Abilities

> **Note:** Replace the `*` in any of the following formulas with one of the ability scores offered by the system:
> `strength`, `dexterity`, `constitution`, `intelligence`, `wisdom`, or `charisma`.

- `@abilities.*.value` - Ability score
- `@abilities.*.mod` - Ability modifier
- `@abilities.*.dc` - DC for this ability, calculated using `8 + proficiency + modifier`

### Attributes

- `@attributes.ac.value` - Current armor class
- `@attributes.attunement.value` - Number of currently attuned items
- `@attributes.attunement.max` - Maximum number of attuned items allowed
- `@attributes.dead.success` - Number of death save successes rolled.
- `@attributes.dead.failure` - Number of death save failures rolled.
- `@attributes.exhaustion` - Current level of exhaustion
- `@attributes.hd` **TODO**
- `@attributes.hp.value` - Current hit points
- `@attributes.hp.damage` - Amount of damage taken
- `@attributes.hp.temp` - Current temporary hit points
- `@attributes.hp.max` - Maximum hit points
- `@attributes.luck.value` - Current number of luck points
- `@attributes.proficiency` - Proficiency bonus

### Skills

> **Note:** Replace the `*` in any of the following formulas with one of the skills offered by the system:
> `acrobatics`, `animalHandling`, `arcana`, `athletics`, `deception`, `history`, `insight`, `intimidation`,
> `investigation`, `medicine`, `nature`, `perception`, `performance`, `persuasion`, `religion`,
> `sleightOfHand`, `stealth`, or `survival`.

- `@proficiencies.skills.*.mod` - Skill modifier
- `@proficiencies.skills.*.passive` - Skill passive value

### Progression

- `@progression.level` - Overall character level
- `@progression.classes.*.levels` - Levels in a specific class, with the class identifier in place of `*`
- `@progression.xp.value` - Current XP
- `@progression.xp.min` - Minimum XP for the character's current level
- `@progression.xp.max` - XP required to advance to next level

### Spellcasting

- `@spellcasting.maxRing` - Maximum spell ring cast-able by the character across all classes


## Item Properties

- `@item.ring.value` - Ring at which a spell is being cast
- `@mod` - Modifier for the primary ability associated with the item
- `@prof` - Proficiency for the item
