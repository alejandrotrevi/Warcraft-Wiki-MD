# API GetMerchantItemInfo

**Contributor:** Lansmi

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
{{deprecatedapi|patch=11.0.5}}
Returns info for a merchant item.
 name, texture, price, quantity, numAvailable, isPurchasable, isUsable, extendedCost, currencyID, spellID = GetMerchantItemInfo(index)

==Arguments==
:;index:{{apitype|number}} - The index of the item in the merchant's inventory

==Returns==
:;name:{{apitype|string}} - The name of the item
:;texture:{{apitype|fileID}} - The texture that represents the item's icon
:;price:{{apitype|number}} - The price of the item (in copper)
:;quantity:{{apitype|number}} - The quantity that will be purchased (the ''batch size'', e.g. 5 for vials)
:;numAvailable:{{apitype|number}} - The number of this item that the merchant has in stock. -1 for unlimited stock.
:;isPurchasable:{{apitype|boolean}}
:;isUsable:{{apitype|boolean}} - True if the player can use this item, false otherwise
:;extendedCost:{{apitype|boolean}} - True if the item has extended (PvP) cost info, false otherwise
:;currencyID:{{apitype|number?}}
:;spellID:{{apitype|number?}}

==Patch changes==
* {{Patch 7.2.0|note=Added isPurchasable.}}

==See also==
*[[API GetMerchantItemCostInfo|GetMerchantItemCostInfo]]
```