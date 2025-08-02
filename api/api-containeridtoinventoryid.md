# API ContainerIDToInventoryID

**Contributor:** Zeal

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
 inventoryID = ContainerIDToInventoryID(containerID)

==Arguments==
:;containerID:{{apitype|number}} - [[BagID]] between 1 and <code>NUM_BAG_SLOTS + NUM_BANKBAGSLOTS</code>

==Returns==
:;inventoryID:{{apitype|number}} - [[InventorySlotId]] used in functions like {{api|PutItemInBag}}() and {{api|GetInventoryItemLink}}()

==Example==
Prints all bag container IDs and their respective inventory IDs<br>(You need to be at the bank for bank inventory IDs to return valid results)
 for i = 1, NUM_BAG_SLOTS + NUM_BANKBAGSLOTS do
     local invID = ContainerIDToInventoryID(i)
     print(i, invID, GetInventoryItemLink("player", invID))
 end

<noinclude>==Values==
{{:API_C_Container.ContainerIDToInventoryID/Values}}</noinclude>
```