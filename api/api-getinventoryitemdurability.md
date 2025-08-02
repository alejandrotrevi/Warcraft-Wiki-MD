# API GetInventoryItemDurability

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the durability of an equipped item.
 current, maximum = GetInventoryItemDurability(invSlotId)

==Arguments==
:;invSlotId:{{apitype|number}} : [[InventorySlotId]]

==Returns==
:;current:{{apitype|number}} - current durability value.
:;maximum:{{apitype|number}} - maximum durability value.

==See also==
* {{api|GetInventorySlotInfo}}
* {{api|GetContainerItemDurability}}
```