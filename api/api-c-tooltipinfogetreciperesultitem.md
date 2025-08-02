# API C TooltipInfo.GetRecipeResultItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TooltipInfo|system=TooltipInfo}}
Needs summary.
 data = C_TooltipInfo.GetRecipeResultItem(recipeID [, craftingReagents [, recraftItemGUID [, recipeLevel [, overrideQualityID]]]])

==Arguments==
:;recipeID:{{apitype|number}}
:;craftingReagents:{{apitype|CraftingReagentInfo[]?}}
{{:Struct CraftingReagentInfo|nocaption=1}}
:;recraftItemGUID:{{apitype|string?}}
:;recipeLevel:{{apitype|number?}}
:;overrideQualityID:{{apitype|number?}}

==Returns==
:;data:{{apitype|TooltipData}}
{{:Struct TooltipData|nocaption=1}}
```