# API C PlayerInfo.GetContentDifficultyCreatureForPlayer

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PlayerInfo|system=PlayerInfo}}
Returns info indicating how much difficulty the player may have if fighting a given unit.
 difficulty = C_PlayerInfo.GetContentDifficultyCreatureForPlayer(unitToken)

==Arguments==
:;unitToken:{{apitype|string}} : [[UnitId]]

==Returns==
:;difficulty:{{apitype|Enum.RelativeContentDifficulty}}
{{:Enum.RelativeContentDifficulty|nocaption=1}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```