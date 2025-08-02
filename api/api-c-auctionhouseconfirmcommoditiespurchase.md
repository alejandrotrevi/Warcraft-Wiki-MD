# API C AuctionHouse.ConfirmCommoditiesPurchase

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Completes a commodity item purchase.
 C_AuctionHouse.ConfirmCommoditiesPurchase(itemID, quantity)

==Arguments==
:;itemID:{{apitype|number}}
:;quantity:{{apitype|number}}

==Details==
* Requires the same <code>itemID</code> and <code>quantity</code> as set in {{api|C_AuctionHouse.StartCommoditiesPurchase}}()

==Example==
{{:API_C_AuctionHouse.StartCommoditiesPurchase}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```