# API C PerksProgram.GetPendingChestRewards

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PerksProgram|system=PerksProgram}}
Needs summary.
 pendingRewards = C_PerksProgram.GetPendingChestRewards()

==Returns==
:;pendingRewards:{{apitype|PerksProgramPendingChestRewards[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| rewardTypeID || {{apitype|number}} || 
|-
| perksVendorItemID || {{apitype|number?}} || 
|-
| rewardAmount || {{apitype|number}} || 
|-
| monthRewarded || {{apitype|string?}} || 
|-
| activityMonthID || {{apitype|number}} || 
|-
| activityThresholdID || {{apitype|number}} || 
|}
```