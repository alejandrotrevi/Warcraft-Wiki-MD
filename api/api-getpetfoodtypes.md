# API GetPetFoodTypes

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the food types the pet can eat.
 food1, ... = GetPetFoodTypes()

==Returns==
:;food1, ...:{{apitype|string}} - A list of food types.

==Details==
* Only seems to return values on Classic.

==Example==
<syntaxhighlight lang="lua">
/dump GetPetFoodTypes() => "Meat", "Fish", "Cheese", "Bread", "Fungus", "Fruit"
</syntaxhighlight>

<!-- luals
---@return string ...
function GetPetFoodTypes() end
-->
```