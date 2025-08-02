# API C EquipmentSet.GetItemIDs

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item IDs of an equipment set.
 itemIDs = C_EquipmentSet.GetItemIDs(equipmentSetID)

==Arguments==
:;equipmentSetID:{{apitype|number}} - Appears to return valid info for indices <code>[0, 2, 4, ...]</code>

==Returns==
:;itemIDs:{{apitype|table}} - a table of numbers indexed by [[InventorySlotId]]

==Example==
To print all items that are part of the first set:
 local items = C_EquipmentSet.GetItemIDs(0)
 for i = 1, 19 do
 	if items[i] then
 		print(i, (GetItemInfo(items[i])))
 	end
 end

{{apinavbox|C_EquipmentSet}}
```