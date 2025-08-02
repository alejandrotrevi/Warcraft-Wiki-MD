# API C Item.RequestLoadItemData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Requests item data and fires {{api|t=e|ITEM_DATA_LOAD_RESULT}}.
 C_Item.RequestLoadItemData(itemLocation)
 C_Item.RequestLoadItemDataByID(itemInfo)

==Arguments==
===<font color="#4ec9b0">RequestLoadItemData</font>===
:;itemLocation:{{apitype|ItemLocationMixin}}
===<font color="#4ec9b0">RequestLoadItemDataByID</font>===
:;itemInfo:{{apitype|string}} : [[ItemLink]] or ID

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```