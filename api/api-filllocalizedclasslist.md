# API FillLocalizedClassList

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.5|removed=11.0.2}}
Fills a table with localized male or female class names.
 tbl = FillLocalizedClassList(tbl [, isFemale])

==Arguments==
:;classTable:{{apitype|table}} - The table you want to be filled with the data.
:;isFemale:{{apitype|boolean?}} - If the table should be filled with female class names.

==Returns==
:;classTable:{{apitype|table}} - The same table argument you passed.

==Example==
Prints all female class names.
<syntaxhighlight lang="lua">
local t = {}
FillLocalizedClassList(t, true)
for classFile, name in pairs(t) do
	print(classFile, name)
end
</syntaxhighlight>

FrameXML already populates the <code>LOCALIZED_CLASS_NAMES_MALE</code> and <code>LOCALIZED_CLASS_NAMES_FEMALE</code> globals.<sup>[https://github.com/Gethe/wow-ui-source/blob/10.0.0/Interface/FrameXML/Constants.lua#L55]</sup>
<syntaxhighlight lang="lua">
/dump LOCALIZED_CLASS_NAMES_MALE, LOCALIZED_CLASS_NAMES_FEMALE
</syntaxhighlight>
<syntaxhighlight lang="lua">
-- on frFR locale
[1] = {
	DEATHKNIGHT = "Chevalier de la mort",
	DEMONHUNTER = "Chasseur de démons",
	DRUID = "Druide",
	EVOKER = "Évocateur",
	HUNTER = "Chasseur",
	MAGE = "Mage",
	MONK = "Moine",
	PALADIN = "Paladin"
	PRIEST = "Prêtre",
	ROGUE = "Voleur",
	SHAMAN = "Chaman",
	WARLOCK = "Démoniste",
	WARRIOR = "Guerrier",
},
[2] = {
	DEATHKNIGHT = "Chevalier de la mort",
	DEMONHUNTER = "Chasseuse de démons",
	DRUID = "Druidesse",
	EVOKER = "Évocatrice",
	HUNTER = "Chasseresse",
	MAGE = "Mage",
	MONK = "Moniale",
	PALADIN = "Paladin"
	PRIEST = "Prêtresse",
	ROGUE = "Voleuse",
	SHAMAN = "Chamane",
	WARLOCK = "Démoniste",
	WARRIOR = "Guerrière",
}

</syntaxhighlight>

{{apinavbox|Class}}
```