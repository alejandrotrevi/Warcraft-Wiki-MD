# API EJ GetSearchResult

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns search results for the Encounter Journal.
 id, stype, difficultyID, instanceID, encounterID, itemLink = EJ_GetSearchResult(index)

==Arguments==
:;index:{{apitype|number}} - search result index, ascending from 1 to {{api|EJ_GetNumSearchResults}}(). 

==Returns==
:;id:{{apitype|number}} - ID of the matching loot/encounter/creature/section or instance.
:;stype:{{apitype|number}} - result type; ascending from 0 for loot, encounter, creature, section, and instance respectively.
:;difficultyID:{{apitype|number}} : [[DifficultyID]]
:;instanceID:{{apitype|number}} : {{dbc|journalinstance|JournalInstance.ID}}
:;encounterID:{{apitype|number}} : [[JournalEncounterID]]
:;itemLink:{{apitype|string}} : [[ItemLink]]

==Details==
* For item results, <code>id</code> specifies encounter journal loot id (and additional information is available through {{api|EJ_GetLootInfo}}), <code>stype</code> is 0, while <code>instanceID</code> and <code>encounterID</code> specify which encounter the item drops from.

==Patch changes==
* {{Patch 4.2.0|note=Added.}}

==See also==
* {{api|EJ_SetSearch}}
```