# API C TradeSkillUI.CraftEnchant

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Needs summary.
 C_TradeSkillUI.CraftEnchant(recipeSpellID [, numCasts [, craftingReagents [, itemTarget [, applyConcentration]]]])

==Arguments==
:;recipeSpellID:{{apitype|number}}
:;numCasts:{{apitype|number?|default=1}}
:;craftingReagents:{{apitype|CraftingReagentInfo[]?}}
{{:Struct CraftingReagentInfo|nocaption=1}}
:;itemTarget:{{apitype|ItemLocation?}}
:;applyConcentration:{{apitype|boolean?}}

==Patch changes==
* {{Patch 11.0.0|note=Added <code>applyConcentration</code> argument.}}
```