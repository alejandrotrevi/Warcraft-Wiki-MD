# API C ContentTracking.GetBestMapForTrackable

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ContentTracking|system=ContentTracking}}
Needs summary.
 result, mapID = C_ContentTracking.GetBestMapForTrackable(trackableType, trackableID [, ignoreWaypoint])

==Arguments==
:;trackableType:{{apitype|Enum.ContentTrackingType}}
{{:Enum.ContentTrackingType|nocaption=1}}
:;trackableID:{{apitype|number}}
:;ignoreWaypoint:{{apitype|boolean?|default=false}}

==Returns==
:;result:{{apitype|Enum.ContentTrackingResult}}
{{:Enum.ContentTrackingResult|nocaption=1}}
:;mapID:{{apitype|number?}}
```