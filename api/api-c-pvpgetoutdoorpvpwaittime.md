# API C PvP.GetOutdoorPvPWaitTime

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the time until the next battle in a PvP zone like Wintergrasp and Tol Barad.
 pvpWaitTime = C_PvP.GetOutdoorPvPWaitTime(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;pvpWaitTime:{{apitype|number}} - seconds until the battle starts.

==Details==
* This will only return a good value if the map is zoned on an outdoor battle map and you are not in an instance.

==Patch changes==
* {{Patch 8.0.1|note=Moved to {{api|C_PvP.GetOutdoorPvPWaitTime}}.}}
* {{Patch 3.2.0|note=Added as {{api|GetOutdoorPVPWaitTime}}.}}
```