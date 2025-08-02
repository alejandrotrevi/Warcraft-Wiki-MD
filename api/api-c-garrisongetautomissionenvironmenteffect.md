# API C Garrison.GetAutoMissionEnvironmentEffect

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Garrison|system=GarrisonInfo}}
Needs summary.
 autoMissionEnvEffect = C_Garrison.GetAutoMissionEnvironmentEffect(missionID)

==Arguments==
:;missionID:{{apitype|number}}

==Returns==
:;autoMissionEnvEffect:{{apitype|AutoMissionEnvironmentEffect?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| autoCombatSpellInfo || {{apitype|AutoCombatSpellInfo}} || 
|}

{{:Struct AutoCombatSpellInfo}}

==Patch changes==
* {{Patch 9.0.2|note=Added.}}
```