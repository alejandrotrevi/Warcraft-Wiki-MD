# API C TradeSkillUI.GetRecipeNumReagents

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Returns the number of distinct reagents needed for the specified recipe.
 numReagents = C_TradeSkillUI.GetRecipeNumReagents(recipeSpellID [, recipeLevel])

==Arguments==
:;recipeSpellID:{{apitype|number}}
:;recipeLevel:{{apitype|number?}}

==Returns==
:;numReagents:{{apitype|number}} - The number of distinct reagents needed for the specified recipe.

==Example==
{{:API_C_TradeSkillUI.GetRecipeReagentInfo}}

==Patch changes==
* {{Patch 10.0.0|note=Removed.}}
* {{Patch 7.0.3|note=Added. Replaces {{api|GetTradeSkillNumReagents}}()}}
```