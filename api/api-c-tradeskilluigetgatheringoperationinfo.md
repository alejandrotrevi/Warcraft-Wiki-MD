# API C TradeSkillUI.GetGatheringOperationInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Needs summary.
 info = C_TradeSkillUI.GetGatheringOperationInfo(recipeID)

==Arguments==
:;recipeID:{{apitype|number}}

==Returns==
:;info:{{apitype|GatheringOperationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| spellID || {{apitype|number}} || 
|-
| maxDifficulty || {{apitype|number}} || 
|-
| baseSkill || {{apitype|number}} || 
|-
| bonusSkill || {{apitype|number}} || 
|-
| bonusStats || {{apitype|GatheringOperationBonusStatInfo[]}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ GatheringOperationBonusStatInfo
! Field !! Type !! Description
|-
| bonusStatName || {{apitype|string}} || 
|-
| bonusStatValue || {{apitype|number}} || 
|-
| ratingDescription || {{apitype|string}} || 
|-
| ratingPct || {{apitype|number}} || 
|-
| bonusRatingPct || {{apitype|number}} || 
|}
```