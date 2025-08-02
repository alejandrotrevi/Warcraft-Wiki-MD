# API C AuctionHouse.GetCancelCost

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns the cost for cancelling a specific owned auction. This is non-zero if it has a bid.
 cancelCost = C_AuctionHouse.GetCancelCost(ownedAuctionID)

==Arguments==
:;ownedAuctionID:{{apitype|number}}

==Returns==
:;cancelCost:{{apitype|number}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```