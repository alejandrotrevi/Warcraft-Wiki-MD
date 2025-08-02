# API GetInventoryItemQuality

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the quality of an equipped item.
 quality = GetInventoryItemQuality(unit, invSlotId)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit whose inventory is to be queried.
:;invSlotId:{{apitype|number}} : [[InventorySlotId]] - The slot ID to be queried, obtained via {{api|GetInventorySlotInfo}}().

==Returns==
:;quality:{{apitype|Enum.ItemQuality}}
```