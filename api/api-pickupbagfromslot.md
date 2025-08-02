# API PickupBagFromSlot

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Picks up the bag from the specified slot, placing it in the cursor.
 PickupBagFromSlot(slot)

==Arguments==
:;slot:{{apitype|number}} - [[API TYPE InventorySlotID|InventorySlotID]] - the slot containing the bag.

==Details==
* Valid slot numbers are 20-23, numbered from left to right starting after the backpack.
* inventoryID ,the result of [[API ContainerIDToInventoryID|ContainerIDtoInventoryID(BagID)]], can help to compute the slot number and bag numbers can be viewed in the [[API TYPE InventorySlotID|InventorySlotID]] page.
```