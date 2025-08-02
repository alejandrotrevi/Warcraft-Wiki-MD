# API C BlackMarket.ItemPlaceBid

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent}}
Places a bid on a black market auction.
 C_BlackMarket.ItemPlaceBid(marketID, bid)

==Arguments==
:;marketID:{{apitype|number}} - black market auction ID ('''not''' line index!) to bid on.
:;bid:{{apitype|number}} - bid amount, in copper.

==Example==
The following snippet bids all your gold on the "Hot Item!" auction.
<syntaxhighlight lang="lua">
local hotMarketID = select(15, C_BlackMarket.GetHotItem())
local allYourGold = GetMoney()
C_BlackMarket.ItemPlaceBid(hotMarketID, allYourGold)
</syntaxhighlight>

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_BlackMarket.GetItemInfoByID}}
```