# API C ContentTracking.IsNavigable

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ContentTracking|system=ContentTracking}}
If successful, returns if the trackable is either on your current map, or if we're able to determine a route to that map from your location via waypoints.
 result, isNavigable = C_ContentTracking.IsNavigable(trackableType, trackableID)

==Arguments==
:;trackableType:{{apitype|Enum.ContentTrackingType}}
{{:Enum.ContentTrackingType|nocaption=1}}
:;trackableID:{{apitype|number}}

==Returns==
:;result:{{apitype|Enum.ContentTrackingResult}}
{{:Enum.ContentTrackingResult|nocaption=1}}
:;isNavigable:{{apitype|boolean}}
```