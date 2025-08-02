# API C TradeSkillUI.GetRecipeReagentItemLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a link for a reagent needed by a recipe.

 itemLink = C_TradeSkillUI.GetRecipeReagentItemLink(recipeId, reagentIndex)

==Arguments==
:;recipeID:{{apitype|number}} -  ID of the recipe to get the reagent link for.
:;reagentIndex:{{apitype|number}} - The index of the reagent to get a link for, between 1 and {{api|C_TradeSkillUI.GetRecipeNumReagents}}(recipeID)..

==Returns==
:;itemLink:{{apitype|string}} - An string containing an [[itemLink]] for the requested reagent.

==Patch changes==
* {{Patch 10.0.0|note=Removed.}}
* {{Patch 7.0.3|note=Added. Replaces {{api|GetTradeSkillReagentItemLink}}.}}

==See also==
* {{api|C_TradeSkillUI.GetRecipeNumReagents}}
* {{api|C_TradeSkillUI.GetRecipeReagentInfo}}
```