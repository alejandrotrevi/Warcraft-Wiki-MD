# API C Item.GetItemInfoInstant

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Returns readily available info for an item.
 itemID, itemType, itemSubType, itemEquipLoc, icon, classID, subClassID = C_Item.GetItemInfoInstant(itemInfo)

==Arguments==
:;item:{{apitype|number,string}} : {{:ItemInfo}}
::* Accepts any valid item ID.
::* Accepts an item link, or minimally in <code>item:%d</code> format.
::* Accepts a localized item name but this requires the item to be or have been in the player's inventory (bags/bank) for that session.

==Returns==
:;itemID:{{apitype|number}} - ID of the item.
:;itemType:{{apitype|string}} : [[ItemType]] - The localized type name of the item: Armor, Weapon, Quest, etc.
:;itemSubType:{{apitype|string}} : [[ItemType]] - The localized sub-type name of the item: Bows, Guns, Staves, etc.
:;itemEquipLoc:{{apitype|string}} : [[Enum.InventoryType|ItemEquipLoc]] - The inventory equipment location in which the item may be equipped e.g. <code>"INVTYPE_HEAD"</code>, or an empty string if it cannot be equipped.
:;icon:{{apitype|fileID}} - The texture for the item icon.
:;classID:{{apitype|number}} : [[ItemType]] - The numeric ID of <code>itemType</code>
:;subClassID:{{apitype|number}} : [[ItemType]] - The numeric ID of <code>itemSubType</code>

==Details==
* This function only returns info that don't require a query to the server. Which has the advantage over {{api|GetItemInfo}}() it will always return data for valid items.

==Example==
* Prints item information for [[Silk Cloth]]
<syntaxhighlight lang="lua">
/dump GetItemInfoInstant(4306)

[1] = 4306,         -- itemID
[2] = "Tradeskill", -- itemType
[3] = "Cloth",      -- itemSubType
[4] = "",           -- itemEquipLoc
[5] = 132905,       -- icon
[6] = 7,            -- classID
[7] = 5             -- subclassID
</syntaxhighlight>

==Patch changes==
* {{Patch 10.2.6|note=Namespaced to <code>C_Item.GetItemInfoInstant</code>.}}
* {{Patch 7.0.3|note=Added.}}
```