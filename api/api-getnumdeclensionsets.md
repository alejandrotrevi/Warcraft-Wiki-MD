# API GetNumDeclensionSets

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of suggested declension sets for a Russian name.
 numDeclensionSets = GetNumDeclensionSets(name, gender)

==Arguments==
:;name:{{apitype|string}}
:;gender:{{apitype|Enum.UnitSex?}}
{{:Enum.UnitSex|nocaption=1}}

==Returns==
:;numDeclensionSets:{{apitype|number}} - Used for {{api|DeclineName}}()

==Details==
* Requires the ruRU client.
* Declension sets are sets of additional names prompted during character creation in the ruRU client.
* Static names for e.g NPCs are in {{dbc|declinedword&locale=ruRU|DeclinedWord.db2}}, {{dbc|declinedwordcases&locale=ruRU|DeclinedWordCases.db2}}
```