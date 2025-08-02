# API GetItemInfoInstant

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns readily available info for an item.
 itemID, itemType, itemSubType, itemEquipLoc, icon, classID, subClassID = GetItemInfoInstant(itemInfo)

==Arguments==
:;item:{{apitype|number,string}} : {{:ItemInfo}}

==Returns==
:;itemID:{{apitype|number}}
:;itemType:{{apitype|string}}
:;itemSubType:{{apitype|string}}
:;itemEquipLoc:{{apitype|string}}
:;icon:{{apitype|fileID}}
:;classID:{{apitype|number}}
:;subClassID:{{apitype|number}}

==Patch changes==
* {{Patch 10.2.6|note=Namespaced to <code>C_Item.GetItemInfoInstant</code>.}}
* {{Patch 7.0.3|note=Added.}}
```