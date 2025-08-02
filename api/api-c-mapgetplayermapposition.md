# API C Map.GetPlayerMapPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}} {{restrictedapi|noinstance}}
Returns the location of the unit on a map.
 position = C_Map.GetPlayerMapPosition(uiMapID, unitToken)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]
:;unitToken:{{apitype|UnitToken}}

==Returns==
:;position:{{apitype|vector2?}}

==Example==
Prints the current map coords for the player.
<syntaxhighlight lang="lua">
local map = C_Map.GetBestMapForUnit("player")
local position = C_Map.GetPlayerMapPosition(map, "player")
print(position:GetXY()) -- 0.54766619205475, 0.54863452911377
</syntaxhighlight>

{{:API_C_Map.GetUserWaypointHyperlink}}
<!-- Sends a message to General chat for the targeted NPC with your current coords.
<syntaxhighlight lang="lua">
/run local m = C_Map.GetPlayerMapPosition(C_Map.GetBestMapForUnit("player"), "player"); SendChatMessage(format("%%t (%d%%) at %.1f, %.1f", UnitHealth("target")/UnitHealthMax("target")*100, m.x*100, m.y*100), "CHANNEL", nil, 1)
</syntaxhighlight>
 > Young Wendigo (100%) at 50.5, 53.4 -->

==Patch changes==
* {{Patch 8.0.1|note=Changed to <code>C_Map.GetPlayerMapPosition()</code> and returns a vector2d.}}
* {{Patch 7.1.0|note=Returns nil while inside a restricted area (instance/battleground/arena).}}
* {{Patch 1.0.0|note=Added as <code>GetPlayerMapPosition()</code>}}

==See also==
* WoWInterface: [https://www.wowinterface.com/forums/showthread.php?t=56290 C_Map.GetPlayerMapPosition Memory Usage]
```