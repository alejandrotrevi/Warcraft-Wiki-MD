# API DeleteCursorItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent,noscript|note=* Limited to deleting a single item per hardware event.}}
Destroys the item held by the cursor.
 DeleteCursorItem()

==Details==
* '''This does not deselect the item, this destroys it.''' Use {{api|t=a|ClearCursor}}() to drop an item from the cursor without destroying it.

==Patch changes==
* {{Patch 9.1.5|note=Protected when called from a (macro) script. Limited to deleting a single item per hardware event.}}
* {{Patch 9.0.2|note=Requires a hardware event. A single hw event is sufficient for destroying multiple items.}}
```