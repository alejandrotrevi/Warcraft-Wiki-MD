# API C AuctionHouse.GetOwnedAuctionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns information for one of the player's active auctions.
 ownedAuction = C_AuctionHouse.GetOwnedAuctionInfo(ownedAuctionIndex)

==Arguments==
:;ownedAuctionIndex:{{apitype|number}}

==Returns==
:;ownedAuction:{{apitype|OwnedAuctionInfo?}}
{{:Struct OwnedAuctionInfo|nocaption=1}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```