# API C Item.IsItemDataCached

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Needs summary.
 isCached = C_Item.IsItemDataCached(itemLocation)
          = C_Item.IsItemDataCachedByID(itemInfo)

==Arguments==
===<font color="#4ec9b0">IsItemDataCached</font>===
:;itemLocation:{{apitype|ItemLocationMixin}}
===<font color="#4ec9b0">IsItemDataCachedByID</font>===
:;itemInfo:{{apitype|string}} : [[ItemLink]] or ID

==Returns==
:;isCached:{{apitype|boolean}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```