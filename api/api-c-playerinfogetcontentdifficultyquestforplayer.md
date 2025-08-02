# API C PlayerInfo.GetContentDifficultyQuestForPlayer

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PlayerInfo|system=PlayerInfo}}
Returns info indicating how much difficulty the player may have when performing a given quest.
 difficulty = C_PlayerInfo.GetContentDifficultyQuestForPlayer(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;difficulty:{{apitype|Enum.RelativeContentDifficulty}}
{{:Enum.RelativeContentDifficulty|nocaption=1}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```