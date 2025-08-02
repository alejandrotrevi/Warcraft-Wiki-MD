# API DeclineName

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns suggested [[wikipedia:Russian_declension#Nouns|declensions]] for a Russian name.
 genitive, dative, accusative, instrumental, prepositional = DeclineName(name, gender?, declensionSet)

==Arguments==
:;name:{{apitype|string}} - Nominative form of the player's or pet's name (string)
:;gender:{{apitype|Enum.UnitSex?}} - Gender for the returned names (for declensions of the player's name, should match the player's gender; for the pet's name, should be neuter).
{{:Enum.UnitSex|nocaption=1}}
:;declensionSet:{{apitype|number}} - Ranging from 1 to {{api|GetNumDeclensionSets}}(). Lower indices correspond to "better" suggestions for the given name.

==Returns==
:;genitive:{{apitype|string}}
:;dative:{{apitype|string}}
:;accusative:{{apitype|string}}
:;instrumental:{{apitype|string}}
:;prepositional:{{apitype|string}}

==Details==
* Requires the ruRU client.
* Static names for e.g NPCs are in {{dbc|declinedword&#38;locale=ruRU|DeclinedWord.db2}}, {{dbc|declinedwordcases&#38;locale=ruRU|DeclinedWordCases.db2}}
```