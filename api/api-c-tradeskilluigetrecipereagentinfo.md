# API C TradeSkillUI.GetRecipeReagentInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Returns the information for a reagent needed by a recipe.
 name, icon, reagentCount, playerReagentCount = C_TradeSkillUI.GetRecipeReagentInfo(recipeSpellID, reagentIndex [, recipeLevel])

==Arguments==
:;recipeSpellID:{{apitype|number}}
:;reagentIndex:{{apitype|number}} - Ranging from 1 to {{api|C_TradeSkillUI.GetRecipeNumReagents}}()
:;recipeLevel:{{apitype|number?}}

==Returns==
:;name:{{apitype|string?}} - The localized name for the reagent.
:;icon:{{apitype|number?}} - Icon [[FileID]]
:;reagentCount:{{apitype|number}} - The required number of the reagent needed to make the recipe once.
:;playerReagentCount:{{apitype|number}} - The amount of the reagent the player has.

==Example==
<onlyinclude>Prints the reagents for [[Thorium Widget]]. The player has 12 Thorium Bars and zero Runecloth.
<syntaxhighlight lang="lua">
local recipeId = 19791 -- Thorium Widget

for i = 1, C_TradeSkillUI.GetRecipeNumReagents(recipeId) do
	print(C_TradeSkillUI.GetRecipeReagentInfo(recipeId, i))
end

-- "Thorium Bar", 133221, 3, 12
-- "Runecloth", 132903, 1, 
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 10.0.0|note=Removed.}}
* {{Patch 7.0.3|note=Added. Replaces {{api|GetTradeSkillReagentInfo}}()}}
```