# API C TradeSkillUI.GetTradeSkillLineForRecipe

**Contributor:** Plusmouse

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MajorFactions|system=MajorFactionsUI}}
Get the associated profession information for a recipe.
 tradeSkillID, skillLineName, parentTradeSkillID = C_TradeSkillUI.GetTradeSkillLineForRecipe(recipeID)

==Arguments==
:;recipeID:{{apitype|number}}

==Returns==
:;tradeSkillID:{{apitype|number}} - skill line ID for profession where recipe comes from (including expansion)
:;skillLineName:{{apitype|string}} - profession name where recipe comes from (including expansion)
:;parentTradeSkillID:{{apitype|number}} - skill line ID for the profession (not expansion specific)
```