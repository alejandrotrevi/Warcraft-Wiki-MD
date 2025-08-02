# API GetInventoryItemLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item link for an equipped item.
 itemLink = GetInventoryItemLink(unit, invSlotId)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit whose inventory is to be queried.
:;invSlotId:{{apitype|number}} : [[InventorySlotId]] - The inventory slot to be queried.

==Returns==
:;itemLink:{{apitype|string?}} : [[ItemLink]] - The item link for the specified item.

==Example==

 local mainHandLink = GetInventoryItemLink("player",GetInventorySlotInfo("MainHandSlot"))
 local _, _, _, _, _, _, itemType = GetItemInfo(mainHandLink)
 DEFAULT_CHAT_FRAME:AddMessage(itemType)

<big>'''Result'''</big>
:Prints the subtype of the mainhand weapon - for example "Mace" or "Sword".
```