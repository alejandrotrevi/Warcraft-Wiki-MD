# API C Garrison.GetAutoTroops

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Garrison|system=GarrisonInfo}}
Needs summary.
 autoTroopInfo = C_Garrison.GetAutoTroops(followerType)

==Arguments==
:;followerType:{{apitype|number}}

==Returns==
:;autoTroopInfo:{{apitype|AutoCombatTroopInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| followerID || {{apitype|string}} || 
|-
| garrFollowerID || {{apitype|string}} || 
|-
| followerTypeID || {{apitype|number}} || 
|-
| displayIDs || {{apitype|FollowerDisplayID[]}} || 
|-
| level || {{apitype|number}} || 
|-
| quality || {{apitype|number}} || 
|-
| levelXP || {{apitype|number}} || 
|-
| maxXP || {{apitype|number}} || 
|-
| height || {{apitype|number}} || 
|-
| scale || {{apitype|number}} || 
|-
| displayScale || {{apitype|number?}} || 
|-
| displayHeight || {{apitype|number?}} || 
|-
| classSpec || {{apitype|number?}} || 
|-
| className || {{apitype|string?}} || 
|-
| flavorText || {{apitype|string?}} || 
|-
| classAtlas || {{apitype|string}} || 
|-
| portraitIconID || {{apitype|number}} || 
|-
| textureKit || {{apitype|string}} || 
|-
| isTroop || {{apitype|boolean}} || 
|-
| raceID || {{apitype|number}} || 
|-
| health || {{apitype|number}} || 
|-
| maxHealth || {{apitype|number}} || 
|-
| role || {{apitype|number}} || 
|-
| isAutoTroop || {{apitype|boolean}} || 
|-
| isSoulbind || {{apitype|boolean}} || <font color="green">9.0.5</font>
|-
| isCollected || {{apitype|boolean}} || 
|-
| autoCombatStats || {{apitype|FollowerAutoCombatStatsInfo}} || 
|}

{{:Struct FollowerDisplayID}}

{{:Struct FollowerAutoCombatStatsInfo}}

==Patch changes==
* {{Patch 9.1.0|note=Removed <code>autoCombatSpells</code> field.}}
* {{Patch 9.0.1|note=Added.}}
```