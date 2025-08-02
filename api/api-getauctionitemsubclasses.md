# API GetAuctionItemSubClasses

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets a list of the sub-classes for an Auction House item class.
 subClass1, subClass2, subClass3, ... = GetAuctionItemSubClasses(classID)

==Arguments==
:;classID:{{apitype|number}} - ID of the item class.

==Returns==
:;subClass1, subClass2, subClass3, ...:{{apitype|number}} - The valid subclasses for an item class.

==Example==
Prints all subclass IDs for the Consumables category.
 local classID = LE_ITEM_CLASS_CONSUMABLE
 for _, subClassID in pairs({GetAuctionItemSubClasses(classID)}) do
 	print(subClassID, (GetItemSubClassInfo(classID, subClassID)))
 end

 0, Explosives and Devices
 1, Potion
 2, Elixir
 3, Flask
 5, Food & Drink
 7, Bandage
 9, Vantus Runes
 8, Other

==See also==
* [[ItemType]] - List of item (sub)classes
* {{api|GetItemClassInfo}}
* {{api|GetItemSubClassInfo}}
* {{api|GetAuctionItemClasses}} (removed)

{{apinavbox|AuctionHouse}}
```