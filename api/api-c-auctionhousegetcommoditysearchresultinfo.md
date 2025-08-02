# API C AuctionHouse.GetCommoditySearchResultInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns search results for a commodity item.
 result = C_AuctionHouse.GetCommoditySearchResultInfo(itemID, commoditySearchResultIndex)

==Arguments==
:;itemID:{{apitype|number}}
:;commoditySearchResultIndex:{{apitype|number}}

==Returns==
:;result:{{apitype|CommoditySearchResultInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| itemID || {{apitype|number}} || 
|-
| quantity || {{apitype|number}} || 
|-
| unitPrice || {{apitype|number}} || 
|-
| auctionID || {{apitype|number}} || 
|-
| owners || {{apitype|string[]}} || 
|-
| totalNumberOfOwners || {{apitype|number}} || 
|-
| timeLeftSeconds || {{apitype|number?}} || 
|-
| numOwnerItems || {{apitype|number}} || 
|-
| containsOwnerItem || {{apitype|boolean}} || 
|-
| containsAccountItem || {{apitype|boolean}} || 
|}

==Example==
{{:API_C_AuctionHouse.SendSearchQuery}}

==Patch changes==
* {{Patch 9.0.5|note=Added <code>totalNumberOfOwners</code> field.}}
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```