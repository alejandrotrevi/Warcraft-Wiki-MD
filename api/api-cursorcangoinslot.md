# API CursorCanGoInSlot

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.0.0|removed=11.0.2}}
Returns true if the item held by the cursor can be equipped in the specified (equipment) inventory slot.
 fitsInSlot = CursorCanGoInSlot(invSlot)

==Arguments==
:;invSlot:{{apitype|number}} : [[inventorySlotId]] - Inventory slot to query

==Returns==
:;fitsInSlot:{{apitype|boolean}} - 1 if the thing currently on the cursor can go into the specified slot, nil otherwise.
```