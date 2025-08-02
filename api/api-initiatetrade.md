# API InitiateTrade

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Opens a trade with the specified unit.
 InitiateTrade(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The player to trade with.

==Related events==
*{{api|t=e|TRADE_ACCEPT_UPDATE}}
*{{api|t=e|TRADE_CLOSED}}
*{{api|t=e|TRADE_MONEY_CHANGED}}
*{{api|t=e|TRADE_PLAYER_ITEM_CHANGED}}
*{{api|t=e|TRADE_REPLACE_ENCHANT}}
*{{api|t=e|TRADE_REQUEST}}
*{{api|t=e|TRADE_REQUEST_CANCEL}}
```