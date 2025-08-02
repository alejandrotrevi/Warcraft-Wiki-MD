# API GetZoneText

**Contributor:** Rhodan46

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of the zone the player is in.
 zoneName = GetZoneText()

==Returns==
:;zoneName:{{apitype|string}} - Localized zone name.

==Details==
* The {{api|t=e|ZONE_CHANGED_NEW_AREA}} is triggered when the main area changes (such as exiting or leaving a major city).
* If you want more detail, {{api|t=e|ZONE_CHANGED}} is also triggered every time you move between sub-sections of an area, (such as going from Shattrath's center to Lower City, etc).
* There is {{api|t=e|ZONE_CHANGED_INDOORS}} for specialized cases.

==Example==
Returns the name of the zone the player is currently in.

 /run print("Current Zone: " .. GetZoneText())

==See also==
* {{api|GetSubZoneText}}()
* {{api|GetRealZoneText}}()
* {{api|GetMinimapZoneText}}()
```