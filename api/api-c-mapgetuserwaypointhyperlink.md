# API C Map.GetUserWaypointHyperlink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns a worldmap hyperlink for the currently assigned user waypoint, if one exists.
 hyperlink = C_Map.GetUserWaypointHyperlink()

==Returns==
:;hyperlink:{{apitype|string}} : [[Hyperlinks#worldmap|worldmapLink]]

==Example==
Sends any currently active waypoint to your chat.
 /run SendChatMessage(C_Map.GetUserWaypointHyperlink())

<onlyinclude>[[File:API_C_Map.GetUserWaypointHyperlink.png|thumb|Sending a map pin for a target]]
Sends a map pin to General chat for the target (but still uses your own location).
<syntaxhighlight lang="lua">
/run local c,p,t,m=C_Map,"player","target"m=c.GetBestMapForUnit(p)c.SetUserWaypoint{uiMapID=m,position=c.GetPlayerMapPosition(m,p)}SendChatMessage(format("%%t (%d%%)%s",UnitHealth(t)/UnitHealthMax(t)*100,c.GetUserWaypointHyperlink()),"CHANNEL",nil,1)
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```