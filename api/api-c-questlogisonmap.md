# API C QuestLog.IsOnMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns true if the specified quest is on the map, and whether or not it has any local PoIs.
 onMap, hasLocalPOI = C_QuestLog.IsOnMap(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;onMap:{{apitype|boolean}}
:;hasLocalPOI:{{apitype|boolean}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```