# API C Garrison.GetFollowerMissionCompleteInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Garrison|system=GarrisonInfo}}
Needs summary.
 followerMissionCompleteInfo = C_Garrison.GetFollowerMissionCompleteInfo(followerID)

==Arguments==
:;followerID:{{apitype|string}} : [[GUID#Follower|FollowerGUID]]

==Returns==
:;followerMissionCompleteInfo:{{apitype|FollowerMissionCompleteInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| displayIDs || {{apitype|FollowerDisplayID[]}} || 
|-
| level || {{apitype|number}} || 
|-
| quality || {{apitype|number}} || 
|-
| currentXP || {{apitype|number}} || 
|-
| maxXP || {{apitype|number}} || 
|-
| height || {{apitype|number}} || 
|-
| scale || {{apitype|number}} || 
|-
| movementType || {{apitype|number?}} || 
|-
| impactDelay || {{apitype|number?}} || 
|-
| castID || {{apitype|number?}} || 
|-
| castSoundID || {{apitype|number?}} || 
|-
| impactID || {{apitype|number?}} || 
|-
| impactSoundID || {{apitype|number?}} || 
|-
| targetImpactID || {{apitype|number?}} || 
|-
| targetImpactSoundID || {{apitype|number?}} || 
|-
| className || {{apitype|string?}} || 
|-
| classAtlas || {{apitype|string}} || 
|-
| portraitIconID || {{apitype|number}} || 
|-
| textureKit || {{apitype|string}} || 
|-
| isTroop || {{apitype|boolean}} || 
|-
| boardIndex || {{apitype|number}} || 
|-
| health || {{apitype|number}} || 
|-
| maxHealth || {{apitype|number}} || 
|-
| role || {{apitype|number}} || 
|}

{{:Struct FollowerDisplayID}}

==Patch changes==
* {{Patch 9.0.1|note=Returns structured data.}}
* {{Patch 6.0.2|note=Added.}}
```