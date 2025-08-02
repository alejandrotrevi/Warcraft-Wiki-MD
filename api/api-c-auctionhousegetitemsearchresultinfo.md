# API C AuctionHouse.GetItemSearchResultInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns search results for an item.
 result = C_AuctionHouse.GetItemSearchResultInfo(itemKey, itemSearchResultIndex)

==Arguments==
:;itemKey:{{apitype|ItemKey}}
{{:Struct ItemKey|nocaption=1}}
:;itemSearchResultIndex:{{apitype|number}}

==Returns==
:;result:{{apitype|ItemSearchResultInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| itemKey || {{apitype|ItemKey}} || 
|-
| owners || {{apitype|string[]}} || 
|-
| totalNumberOfOwners || {{apitype|number}} || 
|-
| timeLeft || {{apitype|Enum.AuctionHouseTimeLeftBand}} || 
|-
| auctionID || {{apitype|number}} || 
|-
| quantity || {{apitype|number}} || 
|-
| itemLink || {{apitype|string?}} || 
|-
| containsOwnerItem || {{apitype|boolean}} || 
|-
| containsAccountItem || {{apitype|boolean}} || 
|-
| containsSocketedItem || {{apitype|boolean}} || 
|-
| bidder || {{apitype|string?}} || 
|-
| minBid || {{apitype|number?}} || 
|-
| bidAmount || {{apitype|number?}} || 
|-
| buyoutAmount || {{apitype|number?}} || 
|-
| timeLeftSeconds || {{apitype|number?}} || 
|}

{{:Enum.AuctionHouseTimeLeftBand}}

==Example==
{{:API_C_AuctionHouse.SendSearchQuery}}

==Patch changes==
* {{Patch 9.0.5|note=Added <code>totalNumberOfOwners</code> field.}}
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```