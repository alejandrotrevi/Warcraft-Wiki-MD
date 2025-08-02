# API GetItemSubClassInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns the name of the item subtype.
 name, isArmorType = GetItemSubClassInfo(classID, subClassID)

==Arguments==
:;classID:{{apitype|number}} - ID of the [[ItemType]]
:;subClassID:{{apitype|number}} - ID of the item subtype

==Returns==
:;name:{{apitype|string}} - Name of the item subtype
:;isArmorType:{{apitype|boolean}} - Seems to only return true for <code>classID 4: Armor - subClassID 0 to 4</code> Miscellaneous, Cloth, Leather,	Mail, Plate

==Example==
Prints the Herbalism subtype for the Profession itemtype.
<syntaxhighlight lang="lua">
print(GetItemSubClassInfo(Enum.ItemClass.Profession, Enum.ItemProfessionSubclass.Herbalism))
-- "Herbalism", false
</syntaxhighlight>

Prints the info of all Profession subtypes.
<syntaxhighlight lang="lua">
for i = Enum.ItemProfessionSubclassMeta.MinValue, Enum.ItemProfessionSubclassMeta.MaxValue do
	print(i, GetItemSubClassInfo(Enum.ItemClass.Profession, i))
end

0, "Blacksmithing", false
1, "Leatherworking", false
2, "Alchemy", false
3, "Herbalism", false
4, "Cooking", false
5, "Mining", false
6, "Tailoring", false
7, "Engineering", false
8, "Enchanting", false
9, "Fishing", false
10, "Skinning", false
11, "Jewelcrafting", false
12, "Inscription", false
13, "Archaeology", false
</syntaxhighlight>

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|GetItemClassInfo}}
* {{api|GetItemInfo}}
```