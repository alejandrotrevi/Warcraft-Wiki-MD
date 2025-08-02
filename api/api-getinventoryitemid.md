# API GetInventoryItemID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item ID for an equipped item.
 itemId, unknown = GetInventoryItemID(unit, invSlotId)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit whose inventory is to be queried.
:;invSlotId:{{apitype|number}} : [[InventorySlotId]] - to be queried, obtained via [[API GetInventorySlotInfo|GetInventorySlotInfo]].

==Returns==
:;itemId:{{apitype|number}} - item id of the item in the inventory slot; nil if there is no item.
:;unknown:{{apitype|number}} - ?
```