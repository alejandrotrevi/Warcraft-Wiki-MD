# API C AreaPoiInfo.GetAreaPOISecondsLeft

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the time left in seconds for an area point of interest.

 secondsLeft = C_AreaPoiInfo.GetAreaPOISecondsLeft(areaPoiID)

==Arguments==
:;areaPoiID:{{apitype|number}} - area point of interest ID.

==Returns==
:;secondsLeft:{{apitype|number}} - time left in seconds.

==Patch changes==
* {{Patch 8.1.5|note=Replaces <code>C_AreaPoiInfo.GetAreaPOITimeLeft()</code><sup>[https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#311]</sup>}}
* {{Patch 8.1.0|note=Added.}}
```