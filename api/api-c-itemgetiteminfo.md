# API C Item.GetItemInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Returns info for an item.
 itemName, itemLink, itemQuality, itemLevel, itemMinLevel, itemType, itemSubType, itemStackCount, itemEquipLoc, itemTexture, sellPrice, classID, subclassID, bindType, expansionID, setID, isCraftingReagent = C_Item.GetItemInfo(itemInfo)

==Arguments==
:;item:{{apitype|ItemInfo}} - {{:ItemInfo}}
::* Accepts any valid item ID but returns <code>nil</code> if the item is not cached yet.
::* Accepts an item link, or minimally in <code>item:%d</code> format.
::* Accepts a localized item name but this requires the item to be or have been in the player's inventory (bags/bank) for that session.

==Returns==
Returns <code>nil</code> if the item is not cached yet or does not exist.
:;1. itemName:{{apitype|string}} - The localized name of the item.
:;2. itemLink:{{apitype|string}} : [[ItemLink]] - The localized link of the item.
:;3. itemQuality:{{apitype|number}} : [[Enum.ItemQuality]] - The quality of the item, e.g. <code>2</code> for [[Uncommon]] and <code>3</code> for [[Rare]] quality items.
:;4. itemLevel:{{apitype|number}} - The base item level, not including upgrades. See {{api|GetDetailedItemLevelInfo}}() for getting the actual item level.
:;5. itemMinLevel:{{apitype|number}} - The minimum level required to use the item, or <code>0</code> if there is no level requirement.
:;6. itemType:{{apitype|string}} : [[ItemType]] - The localized type name of the item: Armor, Weapon, Quest, etc.
:;7. itemSubType:{{apitype|string}} : [[ItemType]] - The localized sub-type name of the item: Bows, Guns, Staves, etc.
:;8. itemStackCount:{{apitype|number}} - The max amount of an item per stack, e.g. 200 for Runecloth.
:;9. itemEquipLoc:{{apitype|string}} : [[Enum.InventoryType|ItemEquipLoc]] - The inventory equipment location in which the item may be equipped e.g. <code>"INVTYPE_HEAD"</code>, or an empty string if it cannot be equipped.
:;10. itemTexture:{{apitype|number}} : [[FileID]] - The texture for the item icon.
:;11. sellPrice:{{apitype|number}} - The vendor price in copper, or <code>0</code> for items that cannot be sold.
:;12. classID:{{apitype|number}} : [[ItemType]] - The numeric ID of <code>itemType</code>
:;13. subclassID:{{apitype|number}} : [[ItemType]] - The numeric ID of <code>itemSubType</code>
:;14. bindType:{{apitype|number}} : [[Enum.ItemBind]] - When the item becomes [[soulbound]], e.g. <code>1</code> for [[Bind on Pickup]] items.
:;15. expansionID:{{apitype|number}} : [[LE_EXPANSION|LE_EXPANSION]] - The related [[Expansion]], e.g. <code>8</code> for Shadowlands. On Classic this appears to be always <code>254</code>.
:;16. setID:{{apitype|number?}} : {{dbc|ItemSet|ItemSetID}} - For example [https://www.wowhead.com/item-set=761/winter-garb 761] for [[Red Winter Hat]] (itemID 21524).
:;17. isCraftingReagent:{{apitype|boolean}} - Whether the item can be used as a [[crafting reagent]].

==Example==
* Prints item information for [[Silk Cloth]]
 /dump GetItemInfo(4306)
<syntaxhighlight lang="lua">
[1] = "Silk Cloth", -- itemName
[2] = "|cffffffff|Hitem:4306::::::::53:258:::::::|h[Silk Cloth]|h|r", -- itemLink
[3] = 1,            -- itemQuality: Enum.ItemQuality.Common
[4] = 13,           -- itemLevel 
[5] = 0,            -- itemMinLevel 
[6] = "Tradeskill", -- itemType 
[7] = "Cloth",      -- itemSubType 
[8] = 200,          -- itemStackCount 
[9] = "",           -- itemEquipLoc
[10] = 132905,      -- itemTexture 
[11] = 150,         -- sellPrice
[12] = 7,           -- classID: LE_ITEM_CLASS_TRADEGOODS
[13] = 5,           -- subclassID 
[14] = 0,           -- bindType: Enum.ItemBind.None
[15] = 0,           -- expansionID: LE_EXPANSION_CLASSIC
[16] = nil,         -- setID
[17] = true         -- isCraftingReagent 
</syntaxhighlight>
{{:ItemMixin}}

==Patch changes==
* {{Patch 10.2.6|note=Namespaced to <code>C_Item.GetItemInfo</code>.}}
* {{Patch 7.1.0|note=Added <code>bindType, expansionID, setID, isCraftingReagent</code> returns.}}
* {{Patch 7.0.3|note=Added <code>classID, subclassID</code> returns. Item icon is now returned as a [[FileID]] rather than a path.}}

==See also==
* {{api|GetItemInfoInstant}}()
```