# API C Item.GetItemStats

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Returns a table of stats for an item.
 statTable = C_Item.GetItemStats(itemLink)

==Arguments==
:;itemLink:{{apitype|string}} - Only accepts an item link, minimally in <code>item:%d</code> format.

==Returns==
:;statTable:{{apitype|table}} - A table whose keys are also [https://www.townlong-yak.com/framexml/10.2.0/GlobalStrings.lua#9909 globalstrings].
<onlyinclude>{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| ITEM_MOD_CRIT_RATING_SHORT || {{apitype|number?}} || Critical Strike
|-
| ITEM_MOD_HASTE_RATING_SHORT|| {{apitype|number?}} || Haste
|-
| ITEM_MOD_INTELLECT_SHORT || {{apitype|number?}} || Intellect
|-
| ITEM_MOD_MASTERY_RATING_SHORT || {{apitype|number?}} || Mastery
|-
| ITEM_MOD_STAMINA_SHORT || {{apitype|number?}} || Stamina
|-
| ITEM_MOD_VERSATILITY || {{apitype|number?}} || Versatility
|-
| RESISTANCE0_NAME || {{apitype|number?}} || Armor
|-
| ... ||  || 
|}</onlyinclude>

==Example==
Dumps an example stat table.
<syntaxhighlight lang="lua">
/dump C_Item.GetItemStats("|cff0070dd|Hitem:137487::::::::70:257::54:6:6652:8812:9302:7756:3268:8766:1:28:628:::::|h[Strand of the Stars]|h|r")

[1]={
	ITEM_MOD_VERSATILITY=508,
	ITEM_MOD_MASTERY_RATING_SHORT=428,
	ITEM_MOD_STAMINA_SHORT=653,
}
</syntaxhighlight>
[[File:API_GetItemStats_02.png|link=]]

Plain item links can be in <code>item:%d</code> format, for example [[Strand of the Stars]].
<syntaxhighlight lang="lua">
/dump C_Item.GetItemStats("item:137487")

[1]={
    ITEM_MOD_VERSATILITY=10,
    ITEM_MOD_MASTERY_RATING_SHORT=8,
    ITEM_MOD_STAMINA_SHORT=5
}
</syntaxhighlight>

Prints the globalstring and value for each stat of an item.
<syntaxhighlight lang="lua">
local stats = C_Item.GetItemStats("|cffa335ee|Hitem:202542::::::::70:257::4:7:6652:9415:9229:9411:9315:1465:8767::::::|h[Mask of the Furnace Seraph]|h|r")

for k, v in pairs(stats) do
	print(format("%s: %d", _G[k], v))
end

-- Armor: 225
-- Intellect: 441
-- Stamina: 1478
-- Critical Strike: 225
-- Haste: 500
</syntaxhighlight>
```