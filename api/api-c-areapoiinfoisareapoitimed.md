# API C AreaPoiInfo.IsAreaPOITimed

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether an area poi is timed.
 isTimed, hideTimerInTooltip = C_AreaPoiInfo.IsAreaPOITimed(areaPoiID)

==Arguments==
:;areaPoiID:{{apitype|number}}

==Returns==
:;isTimed:{{apitype|boolean}}
:;hideTimerInTooltip:{{apitype|boolean?}}

==Details==
* This statically determines if the POI is timed, GetAreaPOITimeLeft retrieves the value from the server and may return nothing for long intervals.

==Patch changes==
* {{Patch 10.1.0|note=Added <code>hideTimerInTooltip</code> return.}}
* {{Patch 8.0.1|note=Added.}}
```