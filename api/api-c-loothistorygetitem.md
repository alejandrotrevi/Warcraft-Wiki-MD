# API C LootHistory.GetItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns item details for a loot event
 rollID, itemLink, numPlayers, isDone, winnerIdx, isMasterLoot = C_LootHistory.GetItem(itemIdx)

==Arguments==
:;idemIdx:{{apitype|number}} - Loot history ID

==Returns==
:;rollID:{{apitype|number}}
:;[[itemLink]]:{{apitype|string}}
:;numPlayers:{{apitype|number}} - Total players eligible for item
:;isDone:{{apitype|boolean}}
:;winnerIdx:{{apitype|number}} - See {{api|C_LootHistory.GetPlayerInfo}}
:;isMasterLoot:{{apitype|boolean}}
```