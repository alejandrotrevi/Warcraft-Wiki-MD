# API GetGuildBankItemInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns item info for a guild bank slot.

 texture, itemCount, locked, isFiltered, quality = GetGuildBankItemInfo(tab,slot)

==Arguments==
:;tab:{{apitype|number}} - The index of the tab in the guild bank
:;slot:{{apitype|number}} - The index of the slot in the chosen tab.

==Returns==
:;texture:{{apitype|number}} - The id of the texture to use for the item. Returns nil if there is no item.
:;itemCount:{{apitype|number}} - The size of the item stack at the chosen slot. Returns 0 if there is no item.
:;locked:{{apitype|boolean}} - Whether or not the slot is locked. Returns nil if it's not locked or the item doesn't exist, 1 otherwise.
:;isFiltered:{{apitype|boolean}} - Returns true if the slot should be hidden because of the users filter, false otherwise.
:;quality:{{apitype|number}} - The quality of the item at the chose slot. Returns nil if there is no item.
```