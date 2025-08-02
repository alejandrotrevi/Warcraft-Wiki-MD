# API GetGuildRecipeInfoPostQuery

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
This function returns information about the last tradeskill you were looking at when you clicked "View Crafters" on a guild listing.
 professionID, recipeID, numMembers = GetGuildRecipeInfoPostQuery()

==Returns==
:;professionID:{{apitype|number}} - this is the same value as would be returned using GetGuildTradeSkillInfo(index)
:;recipeID:{{apitype|number}} - this is the same value as is used by wowhead.com for recipe spells
:;numMembers:{{apitype|number}} - the number of crafters

==Example==
<syntaxhighlight lang="lua">
SelectTradeSkill(index)
QueryGuildMembersForRecipe()
-- in the event handler:
professionID, recipeID, _ = GetGuildRecipeInfoPostQuery()
print("recipe", recipeID, "in profession", professionID, "is now scanned for guildie crafters")
crafter, isOnline = GetGuildRecipeMember(1)
print(crafter, "is the first on the list of crafters for this recipe")
</syntaxhighlight>

<big>Results</big>

recipe 7183 in profession 171 is now scanned for guildie crafters
Bob is the first on the list of crafters for this recipe

==Details==
This function can be used only after the event GUILD_RECIPE_KNOWN_BY_MEMBERS or the client will crash, judging from past performance (without extensive troubleshooting on the use of this particular function).
```