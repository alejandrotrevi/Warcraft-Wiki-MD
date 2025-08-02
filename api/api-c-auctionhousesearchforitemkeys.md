# API C AuctionHouse.SearchForItemKeys

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Queries the auction house for summary results of up to 100 specific items.
 C_AuctionHouse.SearchForItemKeys(itemKeys, sorts)

==Arguments==
:;itemKeys:{{apitype|ItemKey[]}}
{{:Struct AuctionHouse.ItemKey|nocaption=1}}
:;sorts:{{apitype|AuctionHouseSortType[]}}
{{:Struct AuctionHouse.AuctionHouseSortType|nocaption=1}}

==Details==
There is a limit of 100 item keys to be searched for at a time. Searching for more than 100 will often cause a disconnect.

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```