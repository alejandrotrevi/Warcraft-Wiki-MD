# API C AuctionHouse.GetFilterGroups

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns groups of filters for use in the Filter dropdown in the Buy tab.
 filterGroups = C_AuctionHouse.GetFilterGroups()

==Returns==
:;filterGroups:{{apitype|AuctionHouseFilterGroup[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
<!-- |+ [[Struct AuctionHouse.AuctionHouseFilterGroup|AuctionHouseFilterGroup]] -->
! Field !! Type !! Description
|-
| category || {{apitype|Enum.AuctionHouseFilterCategory}} || 
|-
| filters || {{apitype|Enum.AuctionHouseFilter[]}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ Enum.AuctionHouseFilterCategory	
! Value !! Field !! Description
|-
| <center>0</center> || Uncategorized ||
|-
| <center>1</center> || Equipment ||
|-
| <center>2</center> || Rarity ||
|}

{{:Enum_AuctionHouse.AuctionHouseFilter}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```