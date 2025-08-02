# API C TradeSkillUI.GetRecipeDescription

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the description for a recipe.
 recipeDescription = C_TradeSkillUI.GetTradeSkillDescription(recipeID)

==Arguments==
:;recipeID:{{apitype|number}} - Also doubles as a Spell ID.

===Returns===
:;recipeDescription:{{apitype|string}} - For example, "Permanently enchant a two handed melee weapon to grant +25 Agility." Not readily available on function call, see [[SpellMixin#ContinueOnSpellLoad|SpellMixin:ContinueOnSpellLoad]].

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```