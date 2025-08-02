# API GetMinimapZoneText

**Contributor:** Rhodan46

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the zone text that is displayed over the minimap.
 zone = GetMinimapZoneText()

==Returns==
:;zone:{{apitype|string}} - name of the (sub-)zone currently shown above the minimap, e.g. "Trade District".

==Details==
* The {{api|t=e|MINIMAP_ZONE_CHANGED}} event fires when the return value of this function changes.
* The return value equals that of {{api|GetSubZoneText}}() or {{api|GetZoneText}}() depending on whether the player is currently in a named sub-zone or not.

==Example==
Returns the zone name displayed above the minimap

 /run print("Minimap Zone Text: " .. GetMinimapZoneText())

==See also==
* {{api|GetRealZoneText}}()
```