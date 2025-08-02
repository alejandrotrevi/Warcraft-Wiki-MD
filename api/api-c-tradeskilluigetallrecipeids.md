# API C TradeSkillUI.GetAllRecipeIDs

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns all recipes for the current profession.
 recipeIDs = C_TradeSkillUI.GetAllRecipeIDs()

==Returns==
:;recipeIDs:{{apitype|number[]}} - The IDs of all the recipes for the current trade skill, or an empty table if the trade skill panel has yet to be opened.

==Example==
{{:API_C_TradeSkillUI.GetRecipeInfo}}

==Details==
*  The table that is returned includes both learnt and unlearnt recipes and ignores all filtering.

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```