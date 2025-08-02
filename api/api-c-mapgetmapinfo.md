# API C Map.GetMapInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns map information.
 info = C_Map.GetMapInfo(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;info:{{apitype|UiMapDetails}}
{{:Struct Map.UiMapDetails|nocaption=1}}

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|C_Map.GetBestMapForUnit}} }}
{{apirow | Related Events | {{api|t=e|ZONE_CHANGED}}<br>{{api|t=e|ZONE_CHANGED_NEW_AREA}} }}
|}

==Example==
{{:API_C_Map.GetBestMapForUnit#Example}}

==Patch changes==
* {{Patch 8.0.1|note=Added. Replaces <code>GetMapInfo()</code> and {{api|GetMapNameByID}}()}}
```