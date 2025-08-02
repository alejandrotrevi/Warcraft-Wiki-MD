# API EJ GetInstanceForMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns any corresponding instance ID for a UiMapID.
 instanceID = EJ_GetInstanceForMap(mapID)

==Arguments==
:;mapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;instanceID:{{apitype|number}} : {{dbc|journalinstance|JournalInstance.ID}}

==Patch changes==
* {{Patch 8.0.1|note=Added. Replaces {{api|EJ_GetCurrentInstance}}.}}
```