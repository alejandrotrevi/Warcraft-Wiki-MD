# API C EquipmentSet.UseEquipmentSet

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 3.3}}
Equips items from a specified equipment set.
 setWasEquipped = C_EquipmentSet.UseEquipmentSet(equipmentSetID)

==Arguments==
:;equipmentSetID:{{apitype|number}}

==Returns==
:;setWasEquipped:{{apitype|boolean}} - true if the set was equipped, nil otherwise. Failure conditions include invalid arguments, and engaging in combat.

==Details==
* This function does not produce error messages when it fails.
* FrameXML's EquipmentManager_EquipSet("name") will produce a visible error, but will not provide a return value indicating success/failure.

{{apinavbox|C_EquipmentSet}}
```