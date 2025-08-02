# API IsEquippedItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Determines if an item is equipped.
 isEquipped = IsEquippedItem(itemID or itemName)

==Arguments==
:;itemId:{{apitype|number}} - identifier for each unique item
:;itemname:{{apitype|string}} - localized name of an item

==Returns==
:;isEquipped:{{apitype|boolean}} - is item equipped
```