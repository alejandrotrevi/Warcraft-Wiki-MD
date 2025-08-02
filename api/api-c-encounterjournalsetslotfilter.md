# API C EncounterJournal.SetSlotFilter

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_EncounterJournal|system=EncounterJournal}}
Sets the item slot filter for loot items.
 C_EncounterJournal.SetSlotFilter(filterSlot)

==Arguments==
:;filterSlot:{{apitype|Enum.ItemSlotFilterType}}
{{:Enum.ItemSlotFilterType|nocaption=1}}

==Details==
Setting this to <code>Enum.ItemSlotFilterType.NoFilter</code> will reset the filter.

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_EncounterJournal.SetSlotFilter()</code>}}
* {{Patch 7.1.0|note=Added as <code>EJ_SetSlotFilter()</code>}}
```