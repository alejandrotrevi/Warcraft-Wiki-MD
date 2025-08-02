# API C TradeSkillUI.GetRecipeNumItemsProduced

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of items produced for a recipe.
 minMade, maxMade = C_TradeSkillUI.GetRecipeNumItemsProduced(recipeID)

==Parameters==
===Arguments===
:(skillId)

:;skillId:{{apitype|number}} - Which tradeskill to query.
===Returns===
:minMade, maxMade

:;minMade:{{apitype|number}} - The minimum number of items that will be made.
:;maxMade:{{apitype|number}} - The maximum number of items that will be made.

==Patch changes==
* {{Patch 10.0.0|note=Removed.}}
* {{Patch 7.0.3|note=Moved from {{api|GetTradeSkillNumMade}} to {{api| C_TradeSkillUI.GetRecipeNumItemsProduced}}.}}
```