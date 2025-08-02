# API C EquipmentSet.GetEquipmentSetID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the set ID of an equipment set with the specified name.
 equipmentSetID = C_EquipmentSet.GetEquipmentSetID(equipmentSetName)

==Arguments==
:;equipmentSetName:{{apitype|string}} - equipment set name to query

==Returns==
:;equipmentSetID:{{apitype|number}} - set ID of an equipment set with the specified name, or nil if no sets with the specified name are currently saved.

==Patch changes==
* {{Patch 7.2.0|note=Added.}}

{{apinavbox|C_EquipmentSet}}
```