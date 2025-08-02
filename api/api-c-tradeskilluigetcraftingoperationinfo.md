# API C TradeSkillUI.GetCraftingOperationInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Needs summary.
 info = C_TradeSkillUI.GetCraftingOperationInfo(recipeID, craftingReagents, [allocationItemGUID], applyConcentration)

==Arguments==
:;recipeID:{{apitype|number}}
:;craftingReagents:{{apitype|CraftingReagentInfo[]}}
{{:Struct CraftingReagentInfo|nocaption=1}}
:;allocationItemGUID:{{apitype|WOWGUID?}}
:;applyConcentration:{{apitype|boolean}}

==Returns==
:;info:{{apitype|CraftingOperationInfo?}}
{{:Struct CraftingOperationInfo|nocaption=1}}

==Patch changes==
* {{Patch 11.0.0|note=Added <code>applyConcentration</code> argument.}}
```