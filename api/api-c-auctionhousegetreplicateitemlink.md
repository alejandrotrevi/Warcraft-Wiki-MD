# API C AuctionHouse.GetReplicateItemLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns the item link (if loaded) for an item from a [[API C_AuctionHouse.ReplicateItems|ReplicateItems]] result.
 itemLink = C_AuctionHouse.GetReplicateItemLink(index)

==Arguments==
:;index:{{apitype|number}}

==Returns==
:;itemLink:{{apitype|string?}}  - [[ItemLink]]

==Patch changes==
* {{Patch 8.3.0|note=Added. Replaces {{api|GetAuctionItemLink}}(). [https://www.townlong-yak.com/framexml/8.3.0/Blizzard_Deprecated/Deprecated_8_3_0.lua#16]}}

{{apinavbox|C_AuctionHouse}}
```