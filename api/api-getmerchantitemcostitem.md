# API GetMerchantItemCostItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the currency cost for a merchant item.
 itemTexture, itemValue, itemLink, currencyName = GetMerchantItemCostItem(index, itemIndex)

==Arguments==
:;index:{{apitype|number}} - Slot in the merchant's inventory to query.
:;itemIndex:{{apitype|number}} - The index for the required item cost type, ascending from 1 to <code>itemCount</code> returned by {{api|GetMerchantItemCostInfo}}.

==Returns==
:;itemTexture:{{apitype|string}} - The texture that represents the item's icon
:;itemValue:{{apitype|number}} - The number of that item required
:;itemLink:{{apitype|string}} - An [[itemLink]] for the cost item, nil if a currency.
:;currencyName:{{apitype|string}} - Name of the currency required, nil if an item.

==Details==
* <code>itemIndex</code> counts into the number of different "alternate currency" tokens required to buy the item under consideration.  For example, looking at the 25-player Tier 9 vendor, a chestpiece costs 75 Emblems of Triumph and 1 Trophy of the Crusade.  This function would be called with arguments (N,1) to retrieve information about the Emblems and (N,2) to retrieve information about the Trophy, where N is the index of the chestpiece in the merchant window.
```