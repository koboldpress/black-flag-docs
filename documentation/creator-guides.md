---
layout: page
title: Creator Guides
permalink: /documentation/creator-guides
---

![Up to date as of 1.0.053](https://img.shields.io/static/v1?label=black-flag&message=1.0.053&color=informational)

Black Flag provides a number of tools useful to creators putting together compatible modules. Some of these systems, such as the Table of Contents application and registered source books are provided by the system. While other such as DnD5e conversion and text parsing are provided by the [Black Flag Roleplaying Content Tools](https://github.com/koboldpress/black-flag-tools) module.

### DnD5e Content Conversion

The Content Tools module provides tools for converting content from the DnD5e system to the Black Flag system. This tool is necessary due to differences in the data structures of the two systems. Because of the low-level nature of the conversion, the tool requires specific versions of each system to work, usually the latest of each. Check the [releases page](https://github.com/koboldpress/black-flag-tools/releases) for compatibility information for each release of the module. The [conversion tutorial](conversion-tutorial) provides an in-depth guide to this tool.

### Book Parsing

For creating content directly from book text, the Content Tools provides a item parser that can take plain text item blocks from a PDF or text document and convert it into an item in Black Flag. This text parsing works for magic items and spells formatted in the same manner as the officially published source books. The [parsing tutorial](parsing-tutorial) has more details on using this feature.

### Table of Contents

The table of contents system provides an alternate compendium view for Journal compendiums formatted like the table of contents found in source books. Once enabled for a pack and once the appropriate flags are set on the journal pages, the system will handle organizing and displaying a table of contents without any extra code required on the module side. The [table of contents](table-of-contents) covers this system in detail.

### Registered Source Books

The source section on items and NPCs provides a way to link an item back to the book (and even page) where it originated. To avoid having to set the source book manually for each item in a module, the system provides a method for modules to register source books they provide. This is done using a flag in the package manifest (`module.json` or `world.json`) to instruct the system what source books it represents:

```json
{
	"id": "my-cool-module",
	"flags": {
		"black-flag": {
			"sourceBooks": {
				"ToV PG": "Player’s Guide"
			}
		}
	}
}
```

Within the top-level `flags` object in the manifest, add a `black-flag` object and within that add a `sourceBooks` object. Within this object should be key-value pairs of the unique book abbreviation followed by the book's full name. If no easy abbreviation can be made, then feel free to use the full name for both parts, just ensure that the first part is unique for your book.

You can register as many source books as desired and they will all appear as suggestions when using the Configure Identity application in the system, but to take advantage of the automatic book assignment only one should be registered. When the system finds a single source book defined in the manifest, it will automatically assign that book to all content within the compendium packs provided by the module, or imported from those compendium packs.
