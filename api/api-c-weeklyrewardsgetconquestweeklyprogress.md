# API C WeeklyRewards.GetConquestWeeklyProgress

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_WeeklyRewards|system=WeeklyRewards}}
Needs summary.
 weeklyProgress = C_WeeklyRewards.GetConquestWeeklyProgress()

==Returns==
:;weeklyProgress:{{apitype|ConquestWeeklyProgress}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| progress || {{apitype|number}} || 
|-
| maxProgress || {{apitype|number}} || 
|-
| displayType || {{apitype|Enum.ConquestProgressBarDisplayType}} || 
|-
| unlocksCompleted || {{apitype|number}} || 
|-
| maxUnlocks || {{apitype|number}} || 
|-
| sampleItemHyperlink || {{apitype|string}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ Enum.ConquestProgressBarDisplayType
! Value !! Field !! Description
|-
| align="center" | 0 || FirstChest || 
|-
| align="center" | 1 || AdditionalChest || 
|-
| align="center" | 2 || Seasonal || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```