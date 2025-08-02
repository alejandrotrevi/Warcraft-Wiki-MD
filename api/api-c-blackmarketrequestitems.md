# API C BlackMarket.RequestItems

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Requests updated black market auction information from the server.
 C_BlackMarket.RequestItems()

==Triggers events==
* {{api|t=e|BLACK_MARKET_ITEM_UPDATE}}

==Details==
* The black market UI must be open according to the server (i.e. {{api|t=e|BLACK_MARKET_OPEN}} has fired, and {{api|t=e|BLACK_MARKET_CLOSE}} has not fired since) in order for this function to have any effect.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_BlackMarket.GetItemInfoByIndex}}
```