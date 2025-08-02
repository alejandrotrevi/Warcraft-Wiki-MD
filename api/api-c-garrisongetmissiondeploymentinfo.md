# API C Garrison.GetMissionDeploymentInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Garrison|system=GarrisonInfo}}
Needs summary.
 missionDeploymentInfo = C_Garrison.GetMissionDeploymentInfo(missionID)

==Arguments==
:;missionID:{{apitype|number}}

==Returns==
:;missionDeploymentInfo:{{apitype|MissionDeploymentInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| location || {{apitype|string}} || 
|-
| xp || {{apitype|number}} || 
|-
| environment || {{apitype|string?}} || 
|-
| environmentDesc || {{apitype|string?}} || 
|-
| environmentTexture || {{apitype|number}} || 
|-
| locTextureKit || {{apitype|string}} || 
|-
| isExhausting || {{apitype|boolean}} || 
|-
| enemies || {{apitype|GarrisonEnemyEncounterInfo[]}} || 
|}

{{:Struct GarrisonEnemyEncounterInfo}}

==Patch changes==
* {{Patch 9.0.1|note=Changed to <code>C_Garrison.GetMissionDeploymentInfo()</code> and returns structured data.}}
* {{Patch 6.0.2|note=Added as <code>C_Garrison.GetMissionInfo()</code>}}
```