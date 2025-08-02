# API GetShapeshiftFormInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an available form or stance.
 icon, active, castable, spellID = GetShapeshiftFormInfo(index)

==Arguments==
:;index:{{apitype|number}} - index, ascending from 1 to {{api|GetNumShapeshiftForms}}()

==Returns==
:;icon:{{apitype|string}} - Path to icon texture
:;active:{{apitype|boolean}} - 1 if this shapeshift is currently active, nil otherwise
:;castable:{{apitype|boolean}} - 1 if this shapeshift form may be entered, nil otherwise
:;spellID:{{apitype|number}} - ID of the spell that activates this ability

==Details==
* As well as druid shapeshifting, warrior stances, paladin auras, hunter aspects, death knight presences, and shadowform use this API.
```