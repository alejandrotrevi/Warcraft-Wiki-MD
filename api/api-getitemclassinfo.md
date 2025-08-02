# API GetItemClassInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns the name of the item type.
 name = GetItemClassInfo(classID)

==Arguments==
:;classID:{{apitype|number}} - ID of the [[ItemType]]

==Returns==
:;name:{{apitype|string}} - Name of the item type

==Example==
 for i = 0, Enum.ItemClassMeta.NumValues-1 do
 	print(i, GetItemClassInfo(i))
 end

 > 0, Consumable
 > 1, Container
 > 2, Weapon
 > ...

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|GetItemSubClassInfo}}
* {{api|GetItemInfo}}
```