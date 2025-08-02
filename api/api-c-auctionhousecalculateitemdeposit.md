# API C AuctionHouse.CalculateItemDeposit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns required deposit for posting a specific item and quantity.
 depositCost = C_AuctionHouse.CalculateItemDeposit(item, duration, quantity)

==Arguments==
:;item:{{apitype|ItemLocationMixin}}
:;duration:{{apitype|number}} - 1 for 12 hours, 2 for 24 hours, 3 for 48 hours
:;quantity:{{apitype|number}} - quantity of items to auction

==Returns==
:;depositCost:{{apitype|number?}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}
```