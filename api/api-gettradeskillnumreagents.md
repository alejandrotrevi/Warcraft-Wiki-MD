# API GetTradeSkillNumReagents

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of distinct reagents required by the specified recipe. 
 numReagents = GetTradeSkillNumReagents(tradeSkillRecipeId)

==Parameters==
===Arguments===
:;tradeSkillRecipeId:{{apitype|number}} - The id of the trade skill recipe.
===Returns===
:;reagentCount:{{apitype|number}} - The number of distinct reagents required to create the item.


==Example==
 local numReagents = GetTradeSkillNumReagents(id);
 local totalReagents = 0;
 for i=1, numReagents, 1 do
   local reagentName, reagentTexture, reagentCount, playerReagentCount = GetTradeSkillReagentInfo(id, i);
   totalReagents = totalReagents   reagentCount;
 end;
===Result===
Calculates the total number of items required by the recipe.

==Details==
If a recipe calls for 2 copper tubes, 1 malachite and 2 blasting powders, GetTradeSkillNumReagents would return 3. If it required 5 linen cloths, the result would be 1.

Once you know how many distinct reagents you need, you can use [[API GetTradeSkillReagentInfo|GetTradeSkillReagentInfo]] to find out how many of each one are required.
```