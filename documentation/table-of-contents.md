---
layout: page
title: Table of Contents System
permalink: /documentation/table-of-contents
---

The table of contents system allows modules to take advantage of automatic generation of table of contents view for their journal compendiums. There are a few flags that must be set by the module creator in order to take advantage of this system, but once set up the system will handle the rest and no additional code is required from the module.

![Complete table of contents page](/assets/images/table-of-contents/complete.jpg)

### Pack Registration

The first set to setting up the ToC is to add a flag to whichever journal compendium pack it should appear for. In your module's manifest (`module.json` or `world.json`) add a `flags` object to the pack definition and add a `display` flag set to `table-of-contents`:

```json
{
	"id": "kp-tov-players-guide",
	"packs": [
		{
			"name": "rules",
			"label": "Player's Guide",
			"system": "black-flag",
			"ownership": {
				"PLAYER": "OBSERVER",
				"ASSISTANT": "OWNER"
			},
			"path": "./packs/rules/",
			"type": "JournalEntry",
			"flags": {
				"display": "table-of-contents"
			}
		}
	]
}
```

Once you have reloaded Foundry to ensure the manifest changes take effect and launched into your world, you should now find that opening the compendium results in a blank page with "Table of Contents" at the top. Perfect! That means everything is working so far, but you will need to set some additional flags to indicate to the system what journal entries should appear in the table of contents and in what order.

![Empty table of contents page](/assets/images/table-of-contents/empty.jpg)

### Setting Journal Entry Flags

By default no journal entries are displayed in the table of contents. There are at least two flags that must be set on a journal entry to make it appear in the correct position:

#### `type` flag

The `type` flag indicates how the journal entry will be sorted and displayed on the ToC. There are three types supported by the system:
- `chapter`: Chapters are sorted first and the entry name is displayed as a large heading. They will automatically list all of their pages below.
- `appendix`: Appendices are sorted last and also displayed as a large header. By default they do not display their individual pages, but that can be overridden using the `showPages` flag (see below).
- `special`: Special is used for journal entries that should appear as if they are pages beneath a chapter or appendix. They also hide their pages by default.

```javascript
const journalEntry = await fromUuid("...");
journalEntry.setFlag("black-flag", "type", "chapter");
```

![Table of contents entry types](/assets/images/table-of-contents/types.jpg)

#### `showPages` flag

The `showPages` flag on entries controls whether the individual pages are listed beneath the entry name in the list with their own links. This defaults to `true` for entries with the `chapter` type, and `false` for entries with the `appendix` or `special` types.

```javascript
const journalEntry = await fromUuid("...");
journalEntry.setFlag("black-flag", "showPages", false);
```

#### `position` flag

The `position` flag is used to control where chapters and appendices appear in the list. It is usually as simple as setting the first chapter to have a `1`, the second chapter to have `2`, and so on. The position is independent between chapters and appendices, so you can have appendix A also have an position of `1`.

```javascript
const journalEntry = await fromUuid("...");
journalEntry.setFlag("black-flag", "position", 1);
```

This flag only has effect for `chapter` and `appendix` entries.

#### `append` & `order` flags

The `append` and `order` flags are used by `special` entries to control where they appear in the final list. The `append` flag specifies which chapter the special entry will be added to. If no `append` is provided, then a special entry will be added after all of the other chapters and appendices as a top-level entry.

**Note**: The `append` flag corresponds to the absolute chapter position starting at `1`, so if you have 5 chapters and 2 appendices, the range of valid values will be 1–7, with 1–5 being the first through fifth chapter, and 6 & 7 being the first and second appendix.

The `order` flag is used when appending a special entry into a list of pages to determine its location relative to the other pages. This number is sorted relative to the sorting value of the other pages in the primary entry, so you may need a unexpectedly large value depending on the sort order of the page set by Foundry.

```javascript
const journalEntry = await fromUuid("...");
journalEntry.setFlag("black-flag", "append", 3);
journalEntry.setFlag("black-flag", "order", 500000);
```

#### `title` flag

The `title` flag allows you to display a different name in the table of contents than you have in the journal entry itself.

```javascript
const journalEntry = await fromUuid("...");
journalEntry.setFlag("black-flag", "title", "Chapter 1: Stuff");
```

### Hiding Individual Pages

Depending on how your journal entries are structured, sometimes it might be desirable to hide an individual page from the table of contents list. For example, in the Player's Guide each chapter begins with an "Introduction" page that contains the key art for the chapter as well as a brief introductory paragraph. This page should not appear within the table of contents, while the rest of the pages in the chapter should.

Hiding a specific page can be done using the `tocHidden` flag on the specific page (there is no way to force a page to be visible if the containing entry doesn't have `showPages` set):

```javascript
const journalPage = await fromUuid("...");
journalPage.setFlag("black-flag", "tocHidden", true);
```
