# API C ArtifactUI.GetRelicInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 name, icon, slotTypeName, link = C_ArtifactUI.GetRelicInfo(relicSlotIndex)
                                = C_ArtifactUI.GetRelicInfoByItemID(itemID)

==Arguments==
===<font color="#4ec9b0">GetRelicInfo</font>===
:;relicSlotIndex:{{apitype|number}}
===<font color="#4ec9b0">GetRelicInfoByItemID</font>===
:;itemID:{{apitype|number}}

==Returns==
:;name:{{apitype|string}}
:;icon:{{apitype|number}}
:;slotTypeName:{{apitype|string}} - Matches the socket identifiers used in the socketing system.
:;link:{{apitype|string}}

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```