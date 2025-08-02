# API GetBuybackItemInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an item that can be bought back from a merchant.
 name, icon, price, quantity, numAvailable, isUsable, isBound = GetBuybackItemInfo(slotIndex)

==Arguments==
:;slotIndex:{{apitype|number}} - The index of a slot in the merchant's buyback inventory, between 1 and {{api|GetNumBuybackItems}}()

==Returns==
:;name:{{apitype|string?}} - The name of the item.
:;icon:{{apitype|fileID?}} - Icon texture of the item.
:;price:{{apitype|number}} - The price, in copper, it will cost to buy the item(s) back.
:;quantity:{{apitype|number}} - The quantity of items in the stack.
:;numAvailable:{{apitype|number}} - The number available.
:;isUsable:{{apitype|boolean}} - True if the item is usable, false otherwise.
:;isBound:{{apitype|boolean?}}

==See also==
{{api|GetNumBuybackItems}}
```