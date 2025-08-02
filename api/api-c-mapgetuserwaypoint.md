# API C Map.GetUserWaypoint

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns the UiMapPoint structure for the currently assigned user waypoint, if one exists.
 point = C_Map.GetUserWaypoint()
       = C_Map.GetUserWaypointFromHyperlink(hyperlink)

==Arguments==
===<font color="#4ec9b0">GetUserWaypoint</font>===
:None

===<font color="#4ec9b0">GetUserWaypointFromHyperlink</font>===
:;hyperlink:{{apitype|string?}} : [[Hyperlinks#worldmap|worldmapLink]]

==Returns==
:;point : [[UiMapPoint]]
{{:UiMapPoint|nocaption=1}}

==Example==
Dumps the currently set waypoint.
 /dump C_Map.GetUserWaypoint()

<syntaxhighlight lang="lua">
{
	uiMapID = 84,
	position = {
		y = 0.71433198451996,
		x = 0.63557040691376
	}
}
</syntaxhighlight>

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```