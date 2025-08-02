# API C Item.GetItemInventoryType

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Needs summary.
 inventoryType = C_Item.GetItemInventoryType(itemLocation)
               = C_Item.GetItemInventoryTypeByID(itemInfo)

==Arguments==
===<font color="#4ec9b0">GetItemInventoryType</font>===
:;itemLocation:{{apitype|ItemLocationMixin}}

===<font color="#4ec9b0">GetItemInventoryTypeByID</font>===
:;itemInfo:{{apitype|number,string}} : {{:ItemInfo}}

==Returns==
:;inventoryType:{{apitype|Enum.InventoryType?}}
{{:Enum.InventoryType}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```