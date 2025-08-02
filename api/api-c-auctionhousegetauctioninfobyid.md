# API C AuctionHouse.GetAuctionInfoByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Needs summary.
 priceInfo = C_AuctionHouse.GetAuctionInfoByID(auctionID)

==Arguments==
:;auctionID:{{apitype|number}}

==Returns==
:;priceInfo:{{apitype|AuctionInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| itemKey || {{apitype|ItemKey}} || 
|-
| itemLink || {{apitype|string?}} || 
|-
| minBid || {{apitype|number?}} || 
|-
| bidAmount || {{apitype|number?}} || 
|-
| buyoutAmount || {{apitype|number?}} || 
|-
| bidder || {{apitype|string?}} || 
|}

{{:Struct ItemKey}}

==Patch changes==
* {{Patch 9.2.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```