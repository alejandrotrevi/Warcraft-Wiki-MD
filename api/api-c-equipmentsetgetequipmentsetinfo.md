# API C EquipmentSet.GetEquipmentSetInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a saved equipment set.
 name, iconFileID, setID, isEquipped, numItems, numEquipped, numInInventory, numLost, numIgnored = C_EquipmentSet.GetEquipmentSetInfo(equipmentSetID)

==Arguments==
:;equipmentSetID:{{apitype|number}} - equipment set ID to query information about.

==Returns==
:;name:{{apitype|string}} - name of the equipment set.
:;iconFileID:{{apitype|number}} - icon texture selected for the equipment set.
:;setID:{{apitype|number}} - equipment set ID.
:;isEquipped:{{apitype|boolean}} - true if all non-ignored slots in the set are currently equipped.
:;numItems:{{apitype|number}} - number of items included in the set.
:;numEquipped:{{apitype|number}} - number of items in the set currently equipped.
:;numInInventory:{{apitype|number}} - number of items in the set currently in the player's bags/bank, if bank is available.
:;numLost:{{apitype|number}} - number of items in the set that are not currently available to the player.
:;numIgnored:{{apitype|number}} - number of inventory slots ignored by the set.

==Details==
* Equipment set IDs are assigned when the set is created and do not change as other sets are added or deleted.

{{apinavbox|C_EquipmentSet}}
```