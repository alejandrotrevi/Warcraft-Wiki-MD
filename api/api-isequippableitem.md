# API IsEquippableItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns true if an item is equipable by the player.
 result = IsEquippableItem(itemId or itemName or itemLink)

==Parameters==
===Arguments===
:(itemId or "itemName" or "[[itemLink]]")

:;itemId:{{apitype|number}} - The numeric ID of the item. ie. 12345
:;itemName:{{apitype|string}} - The Name of the Item, e.g. "Heavy Silk Bandage"
:;[[itemLink]]:{{apitype|string}} - The [[itemLink]], when Shift-Clicking items.

===Returns===
:;result:1 if equip-able, nil otherwise.

==Example==
On a Druid:

 /dump IsEquippableItem("{{loot|epic|Heroes' Dreadnaught Helmet}}")
 1
 /dump IsEquippableItem("{{loot|epic|Heroes' Dreamwalker Headguard}}")
 1
 /dump IsEquippableItem("{{loot|rare|Mr. Pinchy}}")
 nil
```