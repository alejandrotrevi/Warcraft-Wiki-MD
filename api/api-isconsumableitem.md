# API IsConsumableItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns whether an item is consumed when used.
 isConsumable = IsConsumableItem(itemID or itemLink or itemName)

==Arguments==
:;item:Mixed - An item ID (number), item link or item name (string) to query

==Returns==
:;isConsumable:{{apitype|boolean}} - 1 if the item is consumed when used, nil otherwise
```