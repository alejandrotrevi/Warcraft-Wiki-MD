# API GetGuildRecipeMember

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Renders the name and online status of a guild member having a certain recipe.

 name, online = GetGuildRecipeMember(index)

==Arguments==
:;index:{{apitype|number}} - index, beginning with 1, of a list of members who can craft the recipe

==Returns==
:;name:{{apitype|string}} - crafting member name
:;online:{{apitype|boolean}} - if the user is online

==Details==
Unless the client has seen the guild trade window--as in ViewGuildRecipes()--and clicked a recipe and clicked the button '''View&nbsp;Crafters''' this session, this function will crash the client, as of 4.0.3.

Following this, the returns will change only after each click of "View Crafters". QueryGuildMembersForRecipe() effects this change; SelectTradeSkill() can be used to make the selection.
```