# API GetSocketItemBoundTradeable

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the item currently being socketed can be traded to other eligible players (BoP boss loot).
 isBoundTradeable = GetSocketItemBoundTradeable()

==Returns==
:;isBoundTradeable:{{apitype|boolean}} - 1 if the item selected for socketing is BoP but can currently be traded to other eligible players, nil otherwise.

==Details==
* Bind-on-pickup items looted in dungeon and raid instances can be traded with other players present during the encounter the items dropped from within a limited timeframe.
* If you socket gems into a BoP item within its tradable period, the item will cease being tradable.

==See also==
* {{api|GetSocketItemRefundable}}
```