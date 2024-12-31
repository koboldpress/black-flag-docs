---
layout: page
title: Enrichers
permalink: /documentation/enrichers
---

![Up to date as of 1.2.058](https://img.shields.io/static/v1?label=black-flag&message=1.2.058&color=informational)

Enrichers are bits of formatted text that can be used in journal entries, item or activity descriptions, or actor biographies to automatically enhance the text. They can be used to dynamically fetch information from the document they are contained within or to provide a link for rolling.

[Attack](#Attack) | [Calculation/Lookup](#Calculation-Lookup) | [Check](#Check) | [Damage/Heal](#Damage-Heal) | [Reference](#Reference) | [Save](#Save)

### Using This Guide

This guide breaks down the different types of enrichers offered by the system. Each section lists several examples of using the enricher, a table of options that can be provided, and several potential issues that might cause the enricher to not enrich.

The option table describes the options that can be provided to the enricher. Options are used in the enricher in the format of `<name>=<value>`. If the **Inferred** column is checked, then that indicates that the name can be usually left off and only the value used.

If spaces are required within the value, then you must surround it with double quotation marks: `<name>="Two Words"`. The **Assembled** column indicates that that options can be used with spaces without the quotation marks.

The **Formula** column indicates what type of data is accepted for the value. A list and description of the various formats are available in the dropdown below.

<details>
	<summary>Option Formats</summary>
	<ul>
		<li><strong>Boolean</strong>: Either `true` or `false`.</li>
		<li><strong>Choice</strong>: One of several choices that will be described in the option description below the table.</li>
		<li><strong>Formula</strong>: A roll or calculation formula.</li>
		<li><strong>@-Path</strong>: A path referencing a part of a document's data that begins with the `@` symbol, such as can be used in roll formulas. Cannot contain spaces or other calculation details.</li>
		<li><strong>ID</strong>: A 16-digit ID for a document, found by right clicking on the button in the document header.</li>
	</ul>
</details>

## Attack

The attack enricher displays a to hit value and allows using the selected token to roll that attack.

#### Examples

```
// Example: Fixed +5 to hit
[[/attack formula=5]]
[[/attack +5]]

// Example: Link to specific activity on item, using its to hit value
[[/attack activity=jdRTb04FngE1B8cF]]

// Example: Link to first attack activity on item, or to the containing activity if used on an activity description
[[/attack]]
```

#### Options

| Name       | Format  | Inferred  | Assembled |
| ---------- | ------- | --------- | --------- |
| `activity` | ID      |           |           |
| `formula`  | Formula |     ✔︎     |     ✔︎     |

- `activity`: Specify a specific activity by ID on the same item as this enricher
- `formula`: The formula used when rolling to hit

#### Potential Issues
- If no formula is specified and no attack activity is found
- If both a formula and an activity ID are explicitly set
- Invalid to hit formula


## Calculation/Lookup

The calculation and lookup enrichers are designed to fetch data from the document they are contained within, and then either display it as is or perform some sort of numerical calculation on it.

#### Examples

```
// Example: Display a modified perception value on an NPC
[[calc formula="@attributes.perception + 5"]]
[[calc formula=@attributes.perception+5]]
[[calc @attributes.perception + 5]]

// Example: Display an actor's name in lowercase
[[lookup @name lowercase]]

// Example: Display an actor's name with a fallback
[[lookup @name]]{the creature}

// Display a range label on a weapon
[[lookup @labels.range]]
```

#### Calculation Options

| Name       | Format  | Inferred  | Assembled |
| ---------- | ------- | --------- | --------- |
| `formula`  | Formula |     ✔︎     |     ✔︎     |

- `formula`: Formula calculation to perform. Cannot contain any dice values.

#### Lookup Options

| Name       | Format  | Inferred  | Assembled |
| ---------- | ------- | --------- | --------- |
| `path`     | @-Path  |     ✔︎     |     ✔︎     |
| `style`    | Choice  |     ✔︎     |           |

- `path`: Path to the formula to display, see [Roll Formulas](roll-formulas) for a limited list of these paths. If there is no value found at the path (such as looking up the actor name on an item not in an actor), then the enricher will display the original path unless a fallback is provided using the enricher's label
- `style`: Formatting that will be applied to the final value. Can be `capitalize`, `lowercase`, or `uppercase`

#### Potential Issues
- Dice values included in the calculation formula
- Invalid calculation formula


## Check

The check enricher is used to make ability checks with skill, tool, or vehicle proficiency. The enricher includes a "Request Roll" button that appears for GMs to allow them to send a request to players in chat.

The check enricher has several forms (e.g. [[/check]], [[/skill]], [[/tool]], and [[/vehicle]]) that are all treated the same. It is usually recommended you select the form that matches the check needed, but they all behave the same.

#### Examples

```
// Example: Make a dexterity check
[[/check ability=dexterity]]
[[/check dexterity]]
[[/check dex]]

// Example: Add a DC to a dexterity check
[[/check ability=dexterity dc=20]]
[[/check dexterity 20]]
[[/check DC 20 Dexterity]]

// Example: Make an acrobatics check using default ability
[[/check skill=acrobatics]]
[[/check acrobatics]]
[[/skill skill=acrobatics]]
[[/skill acrobatics]]

// Example: Specify an alternate ability on a skill check
[[/skill ability=strength skill=intimidation dc=20]]
[[/skill DC 20 Strength (Intimidation)]]
[[/skill strength intimidation 20]]

// Example: Use a formula for the DC
[[/check int dc=@abilities.charisma.dc]]
[[/check cha dc="8 + @prof"]]

// Example: Tool & Vehicle checks
[[/tool ability=dexterity tool=thieves]]
[[/tool dexterity tool="Thieves' Tools"]]
[[/vehicle ability=strength vehicle=water]]
```

#### Options

| Name       | Format  | Inferred  | Assembled |
| ---------- | ------- | --------- | --------- |
| `ability`  | Choice  |     ✔︎     |           |
| `dc`       | Formula |		 ✔︎     |           |
| `skill`    | Choice  |		 ✔︎     |           |
| `tool`     | Choice  |		 ✔︎     |           |
| `vehicle`  | Choice  |		 ✔︎     |           |

- `ability`: Ability to use with the check
- `dc`: Specific number or formula used for the DC. Formula must not contain dice values. Can only be used inferred with a number, formulas must contains the `dc=` prefix
- `skill`: Skill to roll. If ability isn't specified, then the default ability for that skill will be used
- `tool` & `vehicle`: Tool or vehicle proficiency to use for the roll. Ability must always be specified when using these proficiencies

#### Potential Issues
- No ability specified or able to be inferred from proficiency type
- Skill, tool, or vehicle proficiency specified wasn't found
- Invalid DC formula


## Damage/Heal

The damage enricher displays a damage description and provides a link for rolling that damage with the selected token. The heal enricher is the same but for performing healing.

#### Examples

```
// Example: Simple damage formula
[[/damage formula="1d6 + 2" type=fire]]
[[/damage formula=1d6+2 type=fire]]
[[/damage 1d6 + 2 fire]]

// Example: Displaying average damage
[[/damage formula=2d6 type=radiant average=true]]
[[/damage 2d6 radiant average]]

// Example: Presenting two different damage type options when rolling
[[/damage formula=1d10 type=bludgeoning|slashing]]
[[/damage formula=1d10 type=bludgeoning/slashing]]

// Example: Including two different damage rolls
[[/damage formula="1d6 + 2" type=piercing & formula=1d4 type=fire average=true]]
[[/damage 1d6 + 2 piercing & 1d4 fire average]]

// Example: Standard healing
[[/heal formula="2d4 + 2" type=healing]]
[[/heal formula="2d4 + 2"]]
[[/heal 2d4 + 2 healing]]
[[/heal 2d4 + 2]]
[[/damage formula="2d4 + 2" type=healing]]
[[/damage 2d4 + 2 healing]]

// Example: Temp HP
[[/heal formula=10 type=temp]]
[[/heal 10 temp]]
[[/damage formula=10 type=temp]]
[[/damage 10 temp]]

// Example: Temp Max HP (increase)
[[/heal formula=1d10 type=max]]
[[/heal 1d10 max]]

// Example: Temp Max HP (decrease)
[[/heal formula=1d10 type=max]]
[[/heal 1d10 max]]

// Example: Link to specific activity on item, using its damage or healing formula
[[/damage activity=jdRTb04FngE1B8cF]]
[[/heal activity=jdRTb04FngE1B8cF]]

// Example: Link to first damage activity on item, or to the containing activity if used on an activity description
[[/damage]]

// Example: Link to first heal activity on item, or to the containing activity if used on an activity description
[[/heal]]

// Example: Use a specific attack mode when fetching damage from attack activity
[[/damage activity=jdRTb04FngE1B8cF mode=twoHanded]]
```

#### Options

| Name        | Format  | Inferred  | Assembled | Global    |
| ----------- | ------- | --------- | --------- | --------- |
| `activity`  | ID      |           |           |     ✔︎     |
| `average`   | Boolean |           |           |     ✔︎     |
| `formula`   | Formula |     ✔︎     |     ✔︎     |           |
| `magical`   | Boolean |           |           |     ✔︎     |
| `mode`      | Choice  |           |           |     ✔︎     |
| `type`      | Choice  |     ✔︎     |           |           |

**Note**: The global column indicates options that can be specified within any damage part, but will apply to the whole enriched content (so `[[/damage 1d4 fire & 1d6 magical bludgeoning]]` and `[[/damage 1d4 magical fire & 1d6 bludgeoning]]` are the same).

- `activity`: Specify a specific activity by ID on the same item as this enricher
- `average`: Display the calculated average damage along side the roll in the enriched text (e.g. `7 (2d6) bludgeoning`)
- `formula`: Formula used for the damage roll
- `magical`: Treat all damage from this enricher as magical
- `mode`: Specify an attack mode to use when rolling the damage. Primarily used when rolling directly from an attack activity
- `type`: One or more types of damage

#### Potential Issues
- If no formulas are specified and no activity with damage is found
- If both a formula and an activity ID are explicitly set
- Invalid damage formula


## Reference

The reference enricher is used to refer to specific rules defined by the system, such as damage types, conditions, spell schools, and specific rule entries. It will create a link to the rule entry in the journals with a tooltip displaying the relevant information for the rule. When referencing a condition, it also provides a convenient button for applying that condition to selected tokens.

#### Examples

```
// Example: Reference a condition
&Reference[condition=prone]
&Reference[Prone]
&Reference[prone]

// Example: Reference a condition without the apply button
&Reference[blinded apply=false]

// Example: Reference another rule
&Reference[rule="Difficult Terrain"]
&Reference[Difficult Terrain]
```

#### Options

| Name       | Format  | Inferred  | Assembled |
| ---------- | ------- | --------- | --------- |
| `apply`    | Boolean |           |           |
| Varies     | Choices |     ✔︎     |     ✔︎     |

- `apply`: Usable only when referencing a condition to prevent the apply condition button from appearing
- The rule can be referenced explicitly by rule category if necessary, but it is usually sufficient to just put in the name of the rule being referenced. A list of current rule categories can be found in the disclosure below

<details>
	<summary>Rule Types</summary>
	<p><code>rule</code>, <code>ability</code>, <code>skill</code>, <code>areaOfEffect</code>, <code>condition</code>, <code>creatureTag</code>, <code>creatureType</code>, <code>damageType</code>, <code>healingType</code>, <code>movementType</code>, <code>property</code>, <code>sense</code>, <code>spellComponent</code>, <code>spellSchool</code>, <code>spellSource</code>, <code>spellTag</code></p>
</details>

#### Potential Issues
- Rule isn't found


## Save

The save enricher is used to make a saving throw. The enricher includes a "Request Roll" button that appears for GMs to allow them to send a request to players in chat.

#### Examples

```
// Example: Create a dexterity saving throw
[[/save ability=dexterity]]
[[/save dexterity]]
[[/save DEX]]

// Example: Add a DC to the save
[[/save ability=dexterity dc=20]]
[[/save dexterity 20]]
[[/save DC 20 DEX]]

// Example: Link to specific activity on item, using its save DC
[[/save activity=jdRTb04FngE1B8cF]]

// Example: Link to first save activity on item, or to the containing activity if used on an activity description
[[/save]]
```

#### Options

| Name       | Format  | Inferred  | Assembled |
| ---------- | ------- | --------- | --------- |
| `ability`  | Choice  |     ✔︎     |           |
| `activity` | ID      |           |           |
| `dc`       | Formula |     ✔︎     |           |

- `ability`: Ability to use when making the save, or `false` to indicate that a save without an associated ability should be made
- `activity`: Specify a specific activity by ID on the same item as this enricher
- `dc`: Specific number or formula used for the DC. Formula must not contain dice values. Can only be used inferred with a number, formulas must contains the `dc=` prefix

#### Potential Issues
- If no ability is specified and no save activity is found
- If both an ability and an activity ID are explicitly set
- Invalid DC formula
