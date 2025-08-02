# API GetContainerItemInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an item in a container slot.
 icon, itemCount, locked, quality, readable, lootable, itemLink, isFiltered, noValue, itemID, isBound = GetContainerItemInfo(bagID, slot)

==Arguments==

:;bagID:{{apitype|number}} - [[BagID]] of the bag the item is in, e.g. 0 for your backpack.
:;slot:{{apitype|number}} - index of the slot inside the bag to look up.

==Returns==

:;1. texture:{{apitype|number}} - The icon texture ([[FileID]]) for the item in the specified bag slot.
:;2. itemCount:{{apitype|number}} - The number of items in the specified bag slot.
:;3. locked:{{apitype|boolean}} - True if the item is locked by the server, false otherwise.
:;4. quality:{{apitype|number}} - The [[API_TYPE Quality|Quality]] of the item.
:;5. readable:{{apitype|boolean}} - True if the item can be "read" (as in a book), false otherwise.
:;6. lootable:{{apitype|boolean}} - True if the item is a temporary container containing items that can be looted, false otherwise.
:;7. itemLink:{{apitype|string}} - The [[itemLink]] of the item in the specified bag slot.
:;8. isFiltered:{{apitype|boolean}} - True if the item is grayed-out during the current inventory search, false otherwise.
:;9. noValue:{{apitype|boolean}} - True if the item has no gold value, false otherwise.
:;10. itemID:{{apitype|number}} - The unique ID for the item in the specified bag slot.
:;11. isBound:{{apitype|boolean}} - True if the item is bound to the current character, false otherwise.

==Patch changes==

* {{Patch 8.0.1|note=9th and 10th return values added.}}
* {{Patch 7.0.3|note=First return value changed from a string texture path to a [[fileID]].}}

==See Also==

*{{api|GetItemInfo}}
*{{api|GetItemInfoInstant}}
```