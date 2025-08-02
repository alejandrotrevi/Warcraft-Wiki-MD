# API GetCraftReagentItemLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
This command returns a required reagent (as an [[itemLink]]) for a specific craftable item from the currently visible tradeskill window.

 reagentLink = GetCraftReagentItemLink(index, n)

==Arguments==
:;index:{{apitype|number}} - index of the requested craft recipe, where 1 is the top-most listed recipe.
:;n:{{apitype|number}} - index of the Nth reagent for the recipe, where 1 is the first reagent.

==Returns==
:;reagentLink:{{apitype|string}} - [[itemLink]] for the requested reagent. 

==Details==
* If you specify an invalid index, nil is returned.
* If there is no visible tradeskill window, nil is returned.

==Patch changes==
* {{Patch 3.0.2|note=Removed.}}
```