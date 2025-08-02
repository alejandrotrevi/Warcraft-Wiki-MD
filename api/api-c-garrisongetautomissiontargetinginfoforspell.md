# API C Garrison.GetAutoMissionTargetingInfoForSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Garrison|system=GarrisonInfo}}
Needs summary.
 targetInfo = C_Garrison.GetAutoMissionTargetingInfoForSpell(missionID, autoCombatSpellID, casterBoardIndex)

==Arguments==
:;missionID:{{apitype|number}}
:;autoCombatSpellID:{{apitype|number}}
:;casterBoardIndex:{{apitype|number}}

==Returns==
:;targetInfo:{{apitype|AutoMissionTargetingInfo[]}}
{{:Struct AutoMissionTargetingInfo|nocaption=1}}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```