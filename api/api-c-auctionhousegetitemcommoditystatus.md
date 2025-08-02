# API C AuctionHouse.GetItemCommodityStatus

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns if the item is a commodity, item or neither.
 isCommodity = C_AuctionHouse.GetItemCommodityStatus(item)

==Arguments==
:;item:{{apitype|ItemLocationMixin}}

==Returns==
:;isCommodity:{{apitype|Enum.ItemCommodityStatus}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
<!-- |+ [[Enum AuctionHouse.ItemCommodityStatus|Enum.ItemCommodityStatus]] -->
! Value !! Field !! Description
|-
| align="center" | 0 || Unknown || 
|-
| align="center" | 1 || Item || 
|-
| align="center" | 2 || Commodity || 
|}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```