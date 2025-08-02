# API GetInventoryItemBroken

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if an inventory item has zero durability.
 isBroken = GetInventoryItemBroken(unit, invSlotId)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit whose inventory is to be queried.
:;invSlotId:{{apitype|number}} : [[InventorySlotId]] - to be queried, obtained via [[API GetInventorySlotInfo|GetInventorySlotInfo]].

==Returns==
:;isBroken:{{apitype|boolean}} - Returns true if the specified item is broken, false otherwise.
```