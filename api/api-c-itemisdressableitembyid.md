# API C Item.IsDressableItemByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Returns true if the item is an Armor or Weapon type and false for all other items (Necklace, Trinkets, Rings, Consumables, etc.).
 isDressableItem = C_Item.IsDressableItemByID(itemInfo)

==Arguments==
:;itemInfo:{{apitype|string}}

==Returns==
:;isDressableItem:{{apitype|boolean}}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```