# API C TooltipInfo.GetRecipeResultItemForOrder

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TooltipInfo|system=TooltipInfo}}
Needs summary.
 data = C_TooltipInfo.GetRecipeResultItemForOrder(recipeID [, craftingReagents [, orderID [, recipeLevel [, overrideQualityID]]]])

==Arguments==
:;recipeID:{{apitype|number}}
:;craftingReagents:{{apitype|CraftingReagentInfo[]?}}
{{:Struct CraftingReagentInfo|nocaption=1}}
:;orderID:{{apitype|number?}}
:;recipeLevel:{{apitype|number?}}
:;overrideQualityID:{{apitype|number?}}

==Returns==
:;data:{{apitype|TooltipData}}
{{:Struct TooltipData|nocaption=1}}
```