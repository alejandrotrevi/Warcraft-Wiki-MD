# API C EncounterJournal.GetLootInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_EncounterJournal|system=EncounterJournal}}
Returns info for loot items available from an encounter.
 itemInfo = C_EncounterJournal.GetLootInfo(id)
          = C_EncounterJournal.GetLootInfoByIndex(index [, encounterIndex])

==Arguments==
===<font color="#4ec9b0">GetLootInfo</font>===
:;id:{{apitype|number}}

===<font color="#4ec9b0">GetLootInfoByIndex</font>===
:;index:{{apitype|number}} - Ranging from 1 to {{api|EJ_GetNumLoot}}()
:;encounterIndex:{{apitype|number?}} - Defaults to the currently viewed journal encounter.

==Returns==
:;itemInfo:{{apitype|EncounterJournalItemInfo}}
{{:Struct EncounterJournalItemInfo|nocaption=1}}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_EncounterJournal.GetLootInfo()</code>}}
* {{Patch 4.2.0|note=Added as <code>EJ_GetLootInfo()</code>}}
```