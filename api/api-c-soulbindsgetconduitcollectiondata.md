# API C Soulbinds.GetConduitCollectionData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Soulbinds|system=Soulbinds}}
Needs summary.
 collectionData = C_Soulbinds.GetConduitCollectionData(conduitID)
                = C_Soulbinds.GetConduitCollectionDataAtCursor()
                = C_Soulbinds.GetConduitCollectionDataByVirtualID(virtualID)
==Arguments==
===<font color="#4ec9b0">GetConduitCollectionData</font>===
:;conduitID:{{apitype|number}} : {{dbc|soulbindconduit|SoulbindConduit.ID}}

===<font color="#4ec9b0">GetConduitCollectionDataAtCursor</font>===
:None

===<font color="#4ec9b0">GetConduitCollectionDataByVirtualID</font>===
:;virtualID:{{apitype|number}}

==Returns==
:;collectionData:{{apitype|ConduitCollectionData?}}
{{:Struct ConduitCollectionData|nocaption=1}}

==Patch changes==
* {{Patch 9.0.2|note=Added <code>C_Soulbinds.GetConduitCollectionDataByVirtualID()</code>}}
* {{Patch 9.0.1|note=Added <code>C_Soulbinds.GetConduitCollectionData()</code> and <code>C_Soulbinds.GetConduitCollectionDataAtCursor()</code>}}
```