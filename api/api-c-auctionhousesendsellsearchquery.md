# API C AuctionHouse.SendSellSearchQuery

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}} {{restrictedapi|noscript|note=Otherwise it will brick the AH.}}
Search for all auctions that are variants of a piece of gear, determined a specific item ID.
 C_AuctionHouse.SendSellSearchQuery(itemKey, sorts, separateOwnerItems)

==Arguments==
:;itemKey:{{apitype|ItemKey}}
{{:Struct AuctionHouse.ItemKey|nocaption=1}}
:;sorts:{{apitype|AuctionHouseSortType[]}}
{{:Struct AuctionHouse.AuctionHouseSortType|nocaption=1}}
:;separateOwnerItems:{{apitype|boolean}}

==Details==
* This is unable to be used to query anything other than gear variants for a single piece of gear.
* The itemKey parameter must have the itemLevel, itemSuffix and battlePetSpeciesID properties set to 0, with the itemID property set to the gear's item ID.
* Search queries are restricted to 100 calls per minute. These should not be used to query the entire auction house. See {{api|C_AuctionHouse.ReplicateItems}}(). ItemKey should have its iLVL and suffix cleared before calling.

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

==See also==
* {{api|C_AuctionHouse.SendSearchQuery}}

{{apinavbox|C_AuctionHouse}}
```