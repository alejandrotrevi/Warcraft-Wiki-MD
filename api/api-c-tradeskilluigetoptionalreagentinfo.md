# API C TradeSkillUI.GetOptionalReagentInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Needs summary.
 slots = C_TradeSkillUI.GetOptionalReagentInfo(recipeSpellID [, recipeLevel])

==Arguments==
:;recipeSpellID:{{apitype|number}}
:;recipeLevel:{{apitype|number?}}

==Returns==
:;slots:{{apitype|OptionalReagentSlot[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| requiredSkillRank || {{apitype|number}} || 
|-
| lockedReason || {{apitype|string?}} || 
|-
| slotText || {{apitype|string?}} || 
|-
| options || {{apitype|number[]}} || 
|}

==Patch changes==
* {{Patch 9.2.0|note=Added <code>recipeLevel</code> argument in build 9.2.0 (42979).}}
* {{Patch 9.1.0|note=Added <code>lockedReason</code> field.}}
* {{Patch 9.0.1|note=Added.}}
```