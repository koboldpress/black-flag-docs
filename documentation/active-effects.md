---
layout: page
title: Active Effects
permalink: /documentation/active-effects
---

![Up to date as of 0.10.042](https://img.shields.io/static/v1?label=black-flag&message=0.10.042&color=informational)

## Player Characters

### Ability - Score

Modify the character's ability score.

| Attribute Key                      | Change Mode | Effect Value | Roll Data? |
| ---------------------------------- | ----------- | ------------ | ---------- |
| `system.abilities.[name].value`    | Any         | `number`     | No         |

> <details>
> <summary>Ability Names</summary>
>
> | Ability      | Name            |
> | ------------ | --------------- |
> | Strength     | `strength`      |
> | Dexterity    | `dexterity`     |
> | Constitution | `constitution`  |
> | Wisdom       | `wisdom`        |
> | Intelligence | `intelligence`  |
> | Charisma     | `charisma`      |
>
> Source: `CONFIG.BlackFlag.abilities`
>
> </details>

### Ability - Maximum Score

Increase the maximum score for a certain ability.

| Attribute Key                      | Change Mode | Effect Value | Roll Data? |
| ---------------------------------- | ----------- | ------------ | ---------- |
| `system.abilities.[name].max`      | Any         | `number`     | No         |

### Ability - Save Proficiency

Change the character's ability save proficiency.

| Attribute Key                                            | Change Mode       | Effect Value | Roll Data? |
| -------------------------------------------------------- | ----------------- | ------------ | ---------- |
| `system.abilities.[name].save.proficiency.multiplier`    | Upgrade/Downgrade | `number`     | No         |

### Attunement - Maximum

Increase the maximum number of attunement slots.

| Attribute Key                      | Change Mode | Effect Value | Roll Data? |
| ---------------------------------- | ----------- | ------------ | ---------- |
| `system.attributes.attunement.max` | Any         | `number`     | No         |

### Hit Points - Bonuses

Add a bonuses to HP, either once or for every class level.

| Attribute Key                          | Change Mode | Effect Value | Roll Data? |
| -------------------------------------- | ----------- | ------------ | ---------- |
| `system.attributes.hp.bonuses.overall` | Any         | `number`     | No         |
| `system.attributes.hp.bonuses.level`   | Any         | `number`     | No         |

### Initiative

Set a different ability for initiative or change initiative proficiency.

| Attribute Key                                           | Change Mode       | Effect Value | Roll Data? |
| ------------------------------------------------------- | ----------------- | ------------ | ---------- |
| `system.attributes.initiative.ability`                  | Any               | `string `    | No         |
| `system.attributes.initiative.proficiency.multiplier`   | Upgrade/Downgrade | `number`     | No         |



## NPCs

### Ability - Modifier

Change the NPCs ability modifier.

| Attribute Key                      | Change Mode | Effect Value | Roll Data? |
| ---------------------------------- | ----------- | ------------ | ---------- |
| `system.abilities.[name].mod`      | Any         | `number`     | No         |

> <details>
> <summary>Ability Names</summary>
>
> | Ability      | Name            |
> | ------------ | --------------- |
> | Strength     | `strength`      |
> | Dexterity    | `dexterity`     |
> | Constitution | `constitution`  |
> | Wisdom       | `wisdom`        |
> | Intelligence | `intelligence`  |
> | Charisma     | `charisma`      |
>
> Source: `CONFIG.BlackFlag.abilities`
>
> </details>

### Hit Points - Maximum

Increase the NPC's maximum hit points.

| Attribute Key                      | Change Mode | Effect Value | Roll Data? |
| ---------------------------------- | ----------- | ------------ | ---------- |
| `system.attributes.hp.max`         | Any         | `number`     | No         |



## Shared

### Armor Class - Formulas

Add an additional armor class calculation.

| Attribute Key                      | Change Mode | Effect Value | Roll Data? |
| ---------------------------------- | ----------- | ------------ | ---------- |
| `system.attributes.ac.formulas`    | Add         | `object`     | No         |

```json
// Example: Mage Armor
{ "label": "Mage Armor", "formula": "13 + @abilities.dexterity.mod" }

// Example: Unarmored Defense
{ "label": "Unarmored Defense", "formula": "13 + @abilities.constitution.mod", "armored": false }

// Example: Armor of Shadows
{ "label": "Armor of Shadows", "formula": "13 + @abilities.charisma.mod", "armored": false, "shielded": false }
```

### Armor Class - Values

Modify the flat AC value (such as for Natural Armor) or set an override (ignores formulas).

| Attribute Key                      | Change Mode | Effect Value | Roll Data? |
| ---------------------------------- | ----------- | ------------ | ---------- |
| `system.attributes.ac.flat`        | Any         | `number`     | No         |
| `system.attributes.ac.override`    | Any         | `number`     | No         |

### Languages

Add additional languages, tags, or telepathy distance.

| Attribute Key                      						                 | Change Mode | Effect Value | Roll Data? |
| -------------------------------------------------------------- | ----------- | ------------ | ---------- |
| `system.proficiencies.languages.value`                         | Add         | `[language]` | No         |
| `system.proficiencies.languages.communication.[type].range`    | Any         | `number`     | No         |
| `system.proficiencies.languages.custom` 											 | Add         | `string `    | No         |
| `system.proficiencies.languages.tags`   											 | Add         | `[tag]`      | No         |

> <details>
> <summary>Communication Types</summary>
>
> | Ability      | Name            |
> | ------------ | --------------- |
> | Telepathy    | `telepathy`     |
>
> Source: `CONFIG.BlackFlag.rangedCommunication`
>
> </details>

> <details>
> <summary>Language Tags</summary>
>
> | Ability                   | Name            |
> | ------------------------- | --------------- |
> | Can't Speak               | `cantSpeak`     |
> | Language Known in Life    | `knownInLife`   |
>
> Source: `CONFIG.BlackFlag.languageTags`
>
> </details>

### Movement

Change base movement, modify a movement formula, or add movement tags

| Attribute Key                             | Change Mode | Effect Value | Roll Data? |
| ----------------------------------------- | ----------- | ------------ | ---------- |
| `system.traits.movement.base`             | Any         | `number`     | No         |
| `system.traits.movement.types.[movement]` | Any         | `formula`    | Yes        |
| `system.traits.movement.tags`             | Add         | `[tag]`      | No         |

> <details>
> <summary>Movement Types</summary>
>
> | Ability      | Name            |
> | ------------ | --------------- |
> | Walk         | `walk`          |
> | Climb        | `climb`         |
> | Fly          | `fly`           |
> | Swim         | `swim`          |
> | Burrow       | `burrow`        |
>
> Source: `CONFIG.BlackFlag.movementTypes`
>
> </details>

### Senses

Modify senses distances or add tags.

| Attribute Key                        | Change Mode | Effect Value | Roll Data? |
| ------------------------------------ | ----------- | ------------ | ---------- |
| `system.traits.senses.types.[sense]` | Any         | `formula`    | Yes        |
| `system.traits.senses.tags`          | Add         | `[tag]`      | No         |


> <details>
> <summary>Sense Types</summary>
>
> | Ability      | Name            |
> | ------------ | --------------- |
> | Darkvision   | `darkvision`    |
> | Keensense    | `keensense`     |
> | Tremorsense  | `tremorsense`   |
> | Truesight    | `truesight`     |
>
> Source: `CONFIG.BlackFlag.senses`
>
> </details>

> <details>
> <summary>Sense Tags</summary>
>
> | Ability                         | Name            |
> | ------------------------------- | --------------- |
> | Can't Sense Beyond This Radius  | `cantSense`     |
>
> Source: `CONFIG.BlackFlag.senseTags`
>
> </details>

### Size

Change the creature's size (will not change the token size).

| Attribute Key                      | Change Mode | Effect Value | Roll Data? |
| ---------------------------------- | ----------- | ------------ | ---------- |
| `system.traits.size`               | Any         | [size]       | No         |

> <details>
> <summary>Sizes</summary>
>
> | Ability     | Name         |
> | ----------- | ------------ |
> | Tiny        | `tiny`       |
> | Small       | `small`      |
> | Medium      | `medium`     |
> | Large       | `large`      |
> | Huge        | `huge`       |
> | Gargantuan  | `gargantuan` |
>
> Source: `CONFIG.BlackFlag.sizes`
>
> </details>

### Condition/Damage Resistances/Immunities/Vulnerabilities

TODO


## Modifiers

TODO
