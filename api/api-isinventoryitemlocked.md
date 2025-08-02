# API IsInventoryItemLocked

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether an inventory item is locked, usually as it awaits pending action.
 isLocked = IsInventoryItemLocked(slotId)

==Arguments==
:;slotId:{{apitype|number}} - The [[API TYPE InventorySlotID|slot ID]] used to refer to that slot in the other GetInventory functions.

==Returns==
:;isLocked:{{apitype|boolean}} - true if the slot is locked, false otherwise

==Details==
* PickupInventoryItem on an empty slot will not lock that slot.
* PickupInventoryItem on the ammo slot will not lock that slot.
```