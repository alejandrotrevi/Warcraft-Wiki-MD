# API EquipCursorItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Equips the currently picked up item to a specific inventory slot.
 EquipCursorItem(slot)

==Parameters==
===Arguments===
:;slot:{{apitype|number}} - The [[InventorySlotId]] to place the item into.

==Example==
 EquipCursorItem(GetInventorySlotInfo("HEADSLOT"));
===Result===
Attempts to equip the currently picked up item to the head slot.
```