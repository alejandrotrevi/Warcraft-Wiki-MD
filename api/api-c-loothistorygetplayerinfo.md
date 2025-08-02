# API C LootHistory.GetPlayerInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns player details for a loot event
 name, class, rollType, roll, isWinner, isMe = C_LootHistory.GetPlayerInfo(itemIdx, playerIdx)

==Arguments==
:;idemIdx:{{apitype|number}} - See {{api|C_LootHistory.GetItem}}

==Returns==
:;name:{{apitype|string}}
:;class:{{apitype|string}}
:;rollType:{{apitype|number}} - (0:pass, 1:need, 2:greed, 3:disenchant)
:;roll:{{apitype|number}}
:;isWinner:{{apitype|boolean}}
:;isMe:{{apitype|boolean}}
```