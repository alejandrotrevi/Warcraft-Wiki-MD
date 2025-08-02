# API C PvP.GetLevelUpBattlegrounds

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Returns info indicating the backgrounds available for leveling.
 battlefields = C_PvP.GetLevelUpBattlegrounds(level)

==Arguments==
:;level:{{apitype|number}}

==Returns==
:;battlefields:{{apitype|LevelUpBattlegroundInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| id || {{apitype|number}} || 
|-
| icon || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| isEpic || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```