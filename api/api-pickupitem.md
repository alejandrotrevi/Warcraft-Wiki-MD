# API PickupItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Place the item on the cursor.
 PickupItem(itemID or itemString or itemName or itemLink) 

==Parameters==
===Arguments===
:(itemId or "[[itemString]]" or "itemName" or "[[itemLink]]")

:;itemId:{{apitype|number}} - The numeric ID of the item. ie. 12345
:;[[itemString]]:{{apitype|string}} - The full item ID in string format, e.g. "item:12345:0:0:0:0:0:0:0".
:::Also supports partial [[itemString]]s, by filling up any missing ":x" value with ":0", e.g. "item:12345:0:0:0"
:;itemName:{{apitype|string}} - The Name of the Item, ex: "Hearthstone"
:::The item must have been equiped, in your bags or in your bank once in this session for this to work.
:;[[itemLink]]:{{apitype|string}} - The [[itemLink]], when Shift-Clicking items.

==Example==
 PickupItem(6948)
 PickupItem("item:6948")
 PickupItem("Hearthstone")
 PickupItem(GetContainerItemLink(0, 1))

====Result====
: Picks up the Hearthstone.  4th one picks up the item in backpack slot 1

==Common usage==

PickupItem(link)
```