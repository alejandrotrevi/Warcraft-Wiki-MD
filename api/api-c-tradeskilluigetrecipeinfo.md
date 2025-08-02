# API C TradeSkillUI.GetRecipeInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Returns information for a recipe.
 recipeInfo = C_TradeSkillUI.GetRecipeInfo(recipeSpellID [, recipeLevel])

==Arguments==
:;recipeSpellID:{{apitype|number}}
:;recipeLevel:{{apitype|number?}}

==Returns==
:;recipeInfo:{{apitype|TradeSkillRecipeInfo?}}
{{:Struct TradeSkillRecipeInfo|nocaption=1}}

==Example==
<onlyinclude>The following snippet lists the names of all the recipes for the current trade skill:
<syntaxhighlight lang="lua">
for _, id in pairs(C_TradeSkillUI.GetAllRecipeIDs()) do
	local recipeInfo = C_TradeSkillUI.GetRecipeInfo(id)
	print(recipeInfo.recipeID, recipeInfo.name)
end
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```