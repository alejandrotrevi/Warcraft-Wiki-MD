# API GetInventoryItemGems

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns item ids of the gems socketed in the item in the specified inventory slot.
 gem1, gem2, ... = GetInventoryItemGems(invSlot);

==Arguments==
; invSlot : Number ([[InventorySlotId]]) - Index of the inventory slot to query.

==Returns==
; gem1, gem2, ... : Number - Item ID of the gem(s) socketed within the item in the queried slot.

==Patch changes==
* {{Patch 7.0.3|note=Removed.}}
```