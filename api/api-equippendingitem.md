# API EquipPendingItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Equips the currently pending Bind-on-Equip or Bind-on-Pickup item from the specified inventory slot.
 EquipPendingItem(invSlot)

==Arguments==
:;invSlot:{{apitype|number}} : [[InventorySlotId]] - The slot ID of the item being equipped

==Details==
* When the player attempts to use a Bind-on-Equip or Bind-on-Pickup item for the first time, the game triggers a confirmation dialog. This method appears to be an internal method used by that dialog which equips the item which activated the dialog if accepted.
```