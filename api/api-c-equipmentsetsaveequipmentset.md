# API C EquipmentSet.SaveEquipmentSet

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Saves your currently equipped items into an equipment set.

 C_EquipmentSet.SaveEquipmentSet(equipmentSetID [, icon])

==Arguments==
:;equipmentSetID:{{apitype|number}} - can be retrieved from an existing equipment set by name with {{api|C_EquipmentSet.GetEquipmentSetID}}.
:;icon:{{apitype|string?}} - icon to use for the equipment set. If ommited, the existing icon will be used.
::Accepts both texture names and file IDs, e.g. "INV_Ammo_Snowball", 655708 or "655708"

==Details==
* Can only modify an existing equipment set.

{{apinavbox|C_EquipmentSet}}
```