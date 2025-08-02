# API C BlackMarket.GetNumItems

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of auctions on the [[Black Market Auction House]].
 numItems = C_BlackMarket.GetNumItems()

==Returns==
:;numItems:{{apitype|number}} - number of auctions on the black market.

==Details==
* Note that the black market API sometimes exposes information about recently-completed auctions, so some of those items may already be sold.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_BlackMarket.GetItemInfoByIndex}}
```