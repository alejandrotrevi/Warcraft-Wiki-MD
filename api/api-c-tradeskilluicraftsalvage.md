# API C TradeSkillUI.CraftSalvage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Needs summary.
 C_TradeSkillUI.CraftSalvage(recipeSpellID, [numCasts], itemTarget [, craftingReagents [, applyConcentration]])

==Arguments==
:;recipeSpellID:{{apitype|number}}
:;numCasts:{{apitype|number?|default=1}} - This defaults to 1 if passed <code>nil</code>.
:;itemTarget:{{apitype|ItemLocation}}
:;craftingReagents:{{apitype|CraftingReagentInfo[]?}}
{{:Struct CraftingReagentInfo|nocaption=1}}
:;applyConcentration:{{apitype|boolean?}}

==Patch changes==
* {{Patch 11.0.0|note=Added <code>craftingReagents, applyConcentration</code> arguments.}}
```