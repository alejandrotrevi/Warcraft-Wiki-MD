# API PickupInventoryItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat}}
Picks up / interacts with an equipment slot.
 PickupInventoryItem(slotId)

==Arguments==
:;slotId:{{apitype|number}} : [[InventorySlotId]]

==Details==
:If the cursor is empty, then it will attempt to pick up the item in the slotId.
:If the cursor has an item, then it will attempt to equip the item to the slotId and place the previous slotId item (if any) where the item on cursor orginated.
:If the cursor is in repair or spell-casting mode, it will attempt the action on the slotId.
:You can use [[API GetInventorySlotInfo|GetInventorySlotInfo]] to get the slotId:

==Example==
 /script PickupInventoryItem(GetInventorySlotInfo("MainHandSlot"))
 /script PickupInventoryItem(GetInventorySlotInfo("SecondaryHandSlot"))

The above attempts a main hand/off-hand weapon swap. It will pick up the weapon from the main hand and then pick up the weapon from the off-hand, attempting to equip the main hand weapon to off-hand and sending the off-hand to main hand if possible.
```