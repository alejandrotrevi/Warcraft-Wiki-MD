# API C Map.SetUserWaypoint

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Changes the user-assigned waypoint to the specified location, encoded as a UiMapPoint structure.
 C_Map.SetUserWaypoint(point)

==Arguments==
:;point : [[UiMapPoint]]
{{:UiMapPoint|nocaption=1}}

==Example==
Sets a waypoint on the current player position.
<syntaxhighlight lang="lua">
local mapID = C_Map.GetBestMapForUnit("player")

if C_Map.CanSetUserWaypointOnMap(mapID) then
	local pos = C_Map.GetPlayerMapPosition(mapID, "player")
	local mapPoint = UiMapPoint.CreateFromVector2D(mapID, pos)
	C_Map.SetUserWaypoint(mapPoint)
else
	print("Cannot set waypoints on this map")
end
</syntaxhighlight>

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```