# API GetContainerItemDurability

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the durability of an item in a container slot.
 current, maximum = GetContainerItemDurability(bag, slot)

==Arguments==
:;bag:{{apitype|number}} - [[BagID|Index of the bag slot]] the bag storing the item is in.
:;slot:{{apitype|number}} - Index of the bag slot containing the item to query durability of.

==Returns==
:;current:{{apitype|number}} - current durability value.
:;maximum:{{apitype|number}} - maximum durability value.

==See also==
* {{api|GetInventoryItemDurability}}
```