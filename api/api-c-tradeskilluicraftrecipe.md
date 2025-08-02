# API C TradeSkillUI.CraftRecipe

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}} {{restrictedapi|hwevent}}
Performs the tradeskill a specified number of times.
 C_TradeSkillUI.CraftRecipe(recipeSpellID [, numCasts [, craftingReagents [, recipeLevel [, orderID [, applyConcentration]]]]])

==Arguments==
:;recipeSpellID:{{apitype|number}} - The ID of the tradeskill recipe.
:;numCasts:{{apitype|number?|default=1}}- The number of times to repeat the creation of the specified recipe.
:;craftingReagents:{{apitype|CraftingReagentInfo[]?}}
{{:Struct CraftingReagentInfo|nocaption=1}}
:;recipeLevel:{{apitype|number?}}
:;orderID:{{apitype|BigUInteger?}}
:;applyConcentration:{{apitype|boolean?}}

==Patch changes==
* {{Patch 11.0.0|note=Added <code>applyConcentration</code> argument.}}
* {{Patch 10.0.2|note=Added <code>orderID</code> argument.}}
* {{Patch 10.0.0|note=Changed <code>optionalReagents</code> argument to <code>craftingReagents</code>}}
* {{Patch 7.0.3|note=Moved from {{api|DoTradeSkill}} to {{api| C_TradeSkillUI.CraftRecipe}}()}}
```