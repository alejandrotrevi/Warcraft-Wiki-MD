# API C AuctionHouse.CalculateCommodityDeposit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns required deposit for posting a commodity and quantity.
 depositCost = C_AuctionHouse.CalculateCommodityDeposit(itemID, duration, quantity)

==Arguments==
:;itemID:{{apitype|number}}
:;duration:{{apitype|number}} - 1 for 12 hours, 2 for 24 hours, 3 for 48 hours
:;quantity:{{apitype|number}} - number of items to auction

==Returns==
:;depositCost:{{apitype|number?}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```