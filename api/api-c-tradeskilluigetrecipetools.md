# API C TradeSkillUI.GetRecipeTools

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the required tools for a recipe.
 ... = C_TradeSkillUI.GetRecipeTools(recipeID)

==Returns==
: ListString tools
:;tools:The tools required for the tradeskill

==Example==

Prints the tools required for the tradeskill to the chatwindow.
 print(BuildColoredListString(C_TradeSkillUI.GetRecipeTools(recipeID)))

==Patch changes==
* {{Patch 7.0.3|note=Moved from {{api|GetTradeSkillTools}} to {{api|C_TradeSkillUI.GetRecipeTools}}.}}
```