# API C AuctionHouse.CanCancelAuction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns if the auction can be cancelled. If it can't, load it with [[API C_AuctionHouse.QueryOwnedAuctions|QueryOwnedAuctions]].
 canCancelAuction = C_AuctionHouse.CanCancelAuction(ownedAuctionID)

==Arguments==
:;ownedAuctionID:{{apitype|number}}

==Returns==
:;canCancelAuction:{{apitype|boolean}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```