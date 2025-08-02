# API C WeeklyRewards.GetActivities

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_WeeklyRewards|system=WeeklyRewards}}
Needs summary.
 activities = C_WeeklyRewards.GetActivities([type])

==Arguments==
:;type:{{apitype|Enum.WeeklyRewardChestThresholdType?}}
{{:Enum.WeeklyRewardChestThresholdType|nocaption=1}}

==Returns==
:;activities:{{apitype|WeeklyRewardActivityInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| type || {{apitype|Enum.WeeklyRewardChestThresholdType}} || 
|-
| index || {{apitype|number}} || 
|-
| threshold || {{apitype|number}} || 
|-
| progress || {{apitype|number}} || 
|-
| id || {{apitype|number}} || 
|-
| level || {{apitype|number}} || 
|-
| claimID || {{apitype|number?}} || 
|-
| raidString || {{apitype|string?}} || 
|-
| rewards || {{apitype|WeeklyRewardActivityRewardInfo[]}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ WeeklyRewardActivityRewardInfo
! Field !! Type !! Description
|-
| type || {{apitype|Enum.CachedRewardType}} || 
|-
| id || {{apitype|number}} || 
|-
| quantity || {{apitype|number}} || 
|-
| itemDBID || {{apitype|string?}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.CachedRewardType
! Value !! Field !! Description
|-
| 0 || None || 
|-
| 1 || Item || 
|-
| 2 || Currency || 
|-
| 3 || Quest || 
|}

==Patch changes==
* {{Patch 9.2.0|note=Added <code>raidString</code> field.}}
* {{Patch 9.0.5|note=Added <code>claimID</code> field.}}
* {{Patch 9.0.1|note=Added.}}
```