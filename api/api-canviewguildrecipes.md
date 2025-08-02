# API CanViewGuildRecipes

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__

Checks if the player can view specific guild recipes.

 canView = CanViewGuildRecipes(skillID)

==Arguments==

:;skillID:{{apitype|number}} - The skill ID to view recipes of. See [[API GetGuildTradeSkillInfo|GetGuildTradeSkillInfo]] on how to fetch a skill ID.

==Returns==

:;canView:{{apitype|boolean}} - Returns 1 if the player can promote, nil if not.

==Details==

{{api|QueryGuildRecipes}} must be called for the API to return true. You can then use {{api|ViewGuildRecipes}} to view the guild recipes for the specific skill ID.
```