# API C ContentTracking.GetTrackablesOnMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ContentTracking|system=ContentTracking}}
Needs summary.
 result, trackableMapInfos = C_ContentTracking.GetTrackablesOnMap(trackableType, uiMapID)

==Arguments==
:;trackableType:{{apitype|Enum.ContentTrackingType}}
{{:Enum.ContentTrackingType|nocaption=1}}
:;uiMapID:{{apitype|number}}

==Returns==
:;result:{{apitype|Enum.ContentTrackingResult}}
{{:Enum.ContentTrackingResult|nocaption=1}}
:;trackableMapInfos:{{apitype|ContentTrackingMapInfo[]}}
{{:Struct ContentTrackingMapInfo|nocaption=1}}
```