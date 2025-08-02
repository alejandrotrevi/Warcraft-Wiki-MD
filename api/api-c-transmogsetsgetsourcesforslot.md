# API C TransmogSets.GetSourcesForSlot

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns sources for a transmog set's slot. Only returns valid data for the current class ([[Class_proficiencies|proficiency]]).
 sources = C_TransmogSets.GetSourcesForSlot(transmogSetID, slot)

==Arguments==
:;[[transmogSetID]]:{{apitype|number}}
:;slot:{{apitype|number}} - [[InventorySlotId]]

==Returns==
:;sources:structure - AppearanceSourceInfo[]
{{:Struct_TransmogCollection.AppearanceSourceInfo}}

==Patch changes==
* {{Patch 7.2.0|note=Added.}}
```