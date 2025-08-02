# API C Garrison.GetMissionEncounterIconInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Garrison|system=GarrisonInfo}}
Needs summary.
 missionEncounterIconInfo = C_Garrison.GetMissionEncounterIconInfo(missionID)

==Arguments==
:;missionID:{{apitype|number}}

==Returns==
:;missionEncounterIconInfo:{{apitype|MissionEncounterIconInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| portraitFileDataID || {{apitype|number}} || 
|-
| missionScalar || {{apitype|number}} || 
|-
| isElite || {{apitype|boolean}} || 
|-
| isRare || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>missionScalar</code> field.}}
* {{Patch 9.0.1|note=Added.}}
```