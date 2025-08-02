# API C TradeSkillUI.RecraftRecipe

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Needs summary.
 result = C_TradeSkillUI.RecraftRecipe(itemGUID [, craftingReagents [, removedModifications [, applyConcentration]]])

==Arguments==
:;itemGUID:{{apitype|WOWGUID}}
:;craftingReagents:{{apitype|CraftingReagentInfo[]?}}
{{:Struct CraftingReagentInfo|nocaption=1}}
:;removedModifications:{{apitype|CraftingItemSlotModification[]?}}
{{:Struct CraftingItemSlotModification|nocaption=1}}
:;applyConcentration:{{apitype|boolean?}}

==Returns==
:;result:{{apitype|boolean}}

==Patch changes==
* {{Patch 11.0.0|note=Added <code>applyConcentration</code> argument.}}
* {{Patch 10.1.0|note=Added <code>removedModifications</code> argument.}}
```