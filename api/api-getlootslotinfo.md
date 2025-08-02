# API GetLootSlotInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a loot slot.
 lootIcon, lootName, lootQuantity, currencyID, lootQuality, locked, isQuestItem, questID, isActive = GetLootSlotInfo(slot)

==Arguments==
:;slot:{{apitype|number}} - the index of the loot (1 is the first item, typically coin)

==Returns==
:;lootIcon:{{apitype|string}} - The path of the graphical icon for the item.
:;lootName:{{apitype|string}} - The name of the item.
:;lootQuantity:{{apitype|number}} - The quantity of the item in a stack. ''Note: Quantity for coin is always 0.''
:;currencyID:{{apitype|number}} - The identifying number of the currency loot in slot, if applicable. ''Note: Returns nil for slots with coin and regular items.''
:; lootQuality:{{apitype|number}} The [[Enum.ItemQuality]] code for the item.
:;locked:{{apitype|boolean}} - Whether you are eligible to loot this item or not. Locked items are by default shown tinted red.
:;isQuestItem:{{apitype|boolean}} - Self-explanatory.
:;questID:{{apitype|number}} - The identifying number for the quest.
:;isActive:{{apitype|boolean}} - True if the item starts a quest that you are not currently on.

==Details==
* When returning coin data, the 'quantity' is always 0 and the 'item' contains the amount and text.  It also includes a line break after each type of coin.  The linebreak can be removed by string substitution.
 print("coins: "..string.gsub(item,"\n"," "))

==Patch changes==
* {{Patch 8.0.1|note=Added new fourth return value (currencyID); moved subsequent return values down one}}
==See also==
* {{api|GetLootSourceInfo}}
* {{Api|GetLootSlotLink}}
* {{Api|GetLootSlotType}}
```