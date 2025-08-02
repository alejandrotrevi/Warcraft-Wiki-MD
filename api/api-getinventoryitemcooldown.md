# API GetInventoryItemCooldown

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Get cooldown information for an inventory item.
 start, duration, enable = GetInventoryItemCooldown(unit, invSlotId)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit whose inventory is to be queried.
:;invSlotId:{{apitype|number}} : [[InventorySlotId]] - to be queried, obtained via [[API GetInventorySlotInfo|GetInventorySlotInfo]].

==Returns==
:;start:{{apitype|number}} - The start time of the cooldown period, or 0 if there is no cooldown (or no item in the slot)
:;duration:{{apitype|number}} - The duration of the cooldown period (NOT the remaining time). 0 if the item has no use/cooldown or the slot is empty.
:;enable:{{apitype|number}} - Returns 1 or 0. 1 if the inventory item is capable of having a cooldown, 0 if not.
```