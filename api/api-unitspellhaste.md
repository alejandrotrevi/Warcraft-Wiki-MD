# API UnitSpellHaste

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the current spell haste percentage for a unit.
 spellHastePercent = UnitSpellHaste(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;spellHastePercent:{{apitype|number}} - The spell haste percent for the queried unit. Will return 0 if no valid unitId is provided.

==Example==
Prints the current spell haste percentage modifier for the targeted unit:
 /dump UnitSpellHaste("target")
 > 13.515724182129

You can use this function to get the non-modified cast time of a spell:
 local spellId = 2060 --Greater Heal
 local castTimeWithHaste = select(7,GetSpellInfo(spellId))
 local spellHasteModifier = 1-UnitSpellHaste("player")/100
 local castTimeWithoutHaste = floor(castTimeWithHaste/spellHasteModifier/100)/10
 print(castTimeWithoutHaste)

This should print 2.5 for [[Heal|Greater Heal]].

==Patch changes==
* {{Patch 4.0.6|note=Added.}}
```