# API C WeeklyRewards.GetActivityEncounterInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_WeeklyRewards|system=WeeklyRewards}}
Needs summary.
 info = C_WeeklyRewards.GetActivityEncounterInfo(type, index)

==Arguments==
:;type:{{apitype|Enum.WeeklyRewardChestThresholdType}}
{{:Enum.WeeklyRewardChestThresholdType|nocaption=1}}
:;index:{{apitype|number}}

==Returns==
:;info:{{apitype|WeeklyRewardActivityEncounterInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| encounterID || {{apitype|number}} || 
|-
| bestDifficulty || {{apitype|number}} || 
|-
| uiOrder || {{apitype|number}} || 
|-
| instanceID || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 9.0.5|note=Added.}}
```