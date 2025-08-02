# API GetTradeSkillReagentInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information on reagents for the specified trade skill.
 reagentName, reagentTexture, reagentCount, playerReagentCount = GetTradeSkillReagentInfo(tradeSkillRecipeId, reagentId)

==Parameters==
===Arguments===
:;tradeSkillRecipeId:The Id of the tradeskill recipe
:;reagentId:The Id of the reagent (from 1 to x, where x is the result of calling [[API GetTradeSkillNumReagents|GetTradeSkillNumReagents]])
===Returns===
:;reagentName:{{apitype|string}} - The name of the reagent.
:;reagentTexture:{{apitype|string}} - The texture for the reagent's icon.
:;reagentCount:{{apitype|number}} - The quantity of this reagent required to make one of these items.
:;playerReagentCount:{{apitype|number}} - The quantity of this reagent in the player's inventory.

==Example==
 local numReagents = GetTradeSkillNumReagents(id);
 local totalReagents = 0;
 for i=1, numReagents, 1 do
   local reagentName, reagentTexture, reagentCount, playerReagentCount = GetTradeSkillReagentInfo(id, i);
   totalReagents = totalReagents + reagentCount;
 end;
===Result===
Calculates the total number of items required by the recipe.
```