# API GetTradePlayerItemInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a trade item.
 name, texture, numItems, quality, enchantment, canLoseTransmog = GetTradePlayerItemInfo(id)

==Arguments==
:;id:{{apitype|number}} - The trade slot index to query.

==Returns==
:;name:{{apitype|string}} - The name of the item.
:;texture:{{apitype|number}} : [[FileDataID]] - The icon associated with the item.
:;numItems:{{apitype|number}} - For stackable items, the number of items in the stack.
:;quality:{{apitype|Enum.ItemQuality}} - The quality of the item.
:;enchantment:{{apitype|string}} - The name of any applied enchantment.
:;canLoseTransmog:{{apitype|boolean}} - <code>true</code> if trading this item will cause the player to lose the ability to transmogrify its appearance.
```