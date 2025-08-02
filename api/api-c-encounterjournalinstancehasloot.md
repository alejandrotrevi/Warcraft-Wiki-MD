# API C EncounterJournal.InstanceHasLoot

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether an instance has a loot table in the journal.
 hasLoot = C_EncounterJournal.InstanceHasLoot([journalInstanceID])

==Arguments==
:;journalInstanceID:{{apitype|number?}} : {{dbc|journalinstance|JournalInstance.ID}} - If omitted, defaults to the currently selected instance from {{api|EJ_SelectInstance}}()

==Returns==
:;hasLoot:{{apitype|boolean}}

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```