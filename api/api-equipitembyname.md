# API EquipItemByName

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Equips an item, optionally into a specified slot.
 EquipItemByName(itemId or itemName or itemLink[, slot])

==Parameters==
===Arguments===
:(itemId or "itemName" or "[[itemLink]]"[, [[inventorySlotId|slot]]])

:;itemId:{{apitype|number}} - The numeric ID of the item. ie. 12345
:;itemName:{{apitype|string}} - The name of the item, ie "Worn Dagger". Partial names are valid inputs as well, ie "Worn". If several items with same piece of name exists, the first one found will be equipped.
:;[[itemLink]]:{{apitype|string}} - The [[itemLink]], when Shift-Clicking items.
:;[[inventorySlotId|slot]]:{{apitype|number?}} - The [[InventorySlotId|inventory slot]] to put the item in, obtained via [[API GetInventorySlotInfo|GetInventorySlotInfo()]].

==Changes in 3.3.0==
When in combat this function now "picks up" the item instead of equipping it, similar to [[API_PickupInventoryItem|PickupInventoryItem]].  Out of combat, the function behaves as expected.  This change was made to address the issue of rogues using "poison swapping" addons to increase their DPS.<ref>{{ref web|url=http://forums.worldofwarcraft.com/thread.html?topicId=21042559255&pageNo=1&sid=1#6|title=Blue post confirming 3.3.0 change}}</ref>

==References==
{{reflist}}
```