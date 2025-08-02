# API GetFramesRegisteredForEvent

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns all frames registered for the specified event, in dispatch order.
 frame1, frame2, ... = GetFramesRegisteredForEvent(event)

==Arguments==
:;event:{{apitype|string}} - [[Events|Event]] for which to return registered frames, e.g. "PLAYER_LOGOUT"

==Returns==
:;frame1, frame2, ...:{{apitype|Frame}} - widget registered for the specified event.

==Details==
* The first frame returned will be the first to receive the given event, and likewise the last returned will receive the event last.  A frame can be moved to the end of this event list order by unregistering and then reregistering for the event.
* Currently, frames registered via {{api|t=w|Frame:RegisterAllEvents}} will be returned before all other frames, but they will actually receive events last (as they are used to profile the normal frames' handlers). This suggests that the above ordering is not always reliable. (Last checked 8.3.7)

==Example==
Prints the amount of frames currently registered to PLAYER_ENTERING_WORLD.
<syntaxhighlight lang="lua">
/dump #{GetFramesRegisteredForEvent("PLAYER_ENTERING_WORLD")}
</syntaxhighlight>

The snippet below unregisters the {{api|t=e|PLAYER_LOGOUT}} events from every frame listening for it
<syntaxhighlight lang="lua">
local function unregister(event, widget, ...)
	if widget then
		widget:UnregisterEvent(event)
		return unregister(event, ...)
	end
end

unregister("PLAYER_LOGOUT", GetFramesRegisteredForEvent("PLAYER_LOGOUT"))
</syntaxhighlight>

==Patch changes==
* {{Patch 2.3.0|note=Added.}}

<!-- luals
---@param event FrameEvent
---@return Frame ...
function GetFramesRegisteredForEvent(event) end
-->
```