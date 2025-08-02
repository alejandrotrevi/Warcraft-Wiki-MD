# API C AuctionHouse.GetItemSearchResultsQuantity

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns how many of the item is available on the auction house.
 totalQuantity = C_AuctionHouse.GetItemSearchResultsQuantity(itemKey)

==Arguments==
:;itemKey:{{apitype|ItemKey}}
{{:Struct AuctionHouse.ItemKey|nocaption=1}}

==Returns==
:;totalQuantity:{{apitype|number}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```