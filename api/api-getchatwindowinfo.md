# API GetChatWindowInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a chat window.
 name, fontSize, r, g, b, alpha, shown, locked, docked, uninteractable = GetChatWindowInfo(frameIndex)

==Arguments==
:;frameIndex:{{apitype|number}} - The index of the chat window to get information for (starts at 1).

==Returns==
:;name:{{apitype|string}} - The name of the chat window, or an empty string for its default name.
:;fontSize:{{apitype|number}} - The font size for the window.
:;r:{{apitype|number}} - The red component of the window's background color (0.0 - 1.0);
:;g:{{apitype|number}} - The green component of the window's background color (0.0 - 1.0);
:;b:{{apitype|number}} - The blue component of the window's background color (0.0 - 1.0);
:;alpha:{{apitype|number}} - The alpha level (opacity) of the window background (0.0 - 1.0);
:;shown:{{apitype|boolean}} - true if the window is shown, false if it is hidden.
:;locked:{{apitype|boolean}} - true if the window is locked in place, false if it is movable.
:;docked:{{apitype|number}} - 1 to NUM_CHAT_WINDOWS; Index Order of docked tab EG: General = 1, Combat Log = 2. nil if floating.
:;uninteractable:{{apitype|boolean}} - true if the window should ignore all mouse events; otherwise false

==Details==
* Retrieves Chat Window configuration information. This is what FrameXML uses to know how to display the actual windows. This configuration information is set via the SetChatWindow...() family of functions which causes the "UPDATE_CHAT_WINDOWS" event to fire. FrameXML calls GetChatWindowInfo() when it receives this event.
* 'frameIndex' can be any chat window index between 1 and NUM_CHAT_WINDOWS. '1' is the main chat window.
```