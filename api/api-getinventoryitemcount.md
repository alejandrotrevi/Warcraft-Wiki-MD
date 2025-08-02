# API GetInventoryItemCount

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Determine the quantity of an item in an inventory slot.
 count = GetInventoryItemCount(unit, invSlotId)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit whose inventory is to be queried.
:;invSlotId:{{apitype|number}} : [[InventorySlotId]] - to be queried, obtained via [[API GetInventorySlotInfo|GetInventorySlotInfo]].

==Returns==
:;count:{{apitype|number}} - Returns 1 on empty slots (Thus, on empty ammo slot, 1 is returned). For containers (Bags, etc.), this returns the number of items stored inside the container (Thus, empty containers return 0). Under all other conditions, this function returns the amount of items in the specified slot.

==Example==
<!-- begin code -->
 local ammoSlot = GetInventorySlotInfo("AmmoSlot");
 local ammoCount = GetInventoryItemCount("player", ammoSlot);
 if ((ammoCount == 1) and (not GetInventoryItemTexture("player", ammoSlot))) then
     ammoCount = 0;
 end;
<!-- end code -->
```