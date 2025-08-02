# API SaveView

**Contributor:** LudiusMaximus

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Saves a camera angle. The last position loaded is stored in the [[CVar cameraView]].
 SaveView(viewIndex)

==Arguments==
:;viewIndex:{{apitype|number}} - The index (2-5) to save the camera angle to. (1 is reserved for first person view)

==Details==
* Saved views are preserved across sessions.
* Use ResetView(viewIndex) to reset a view to its default.
* The last position loaded is stored in the [[CVar cameraView]].
* The game's camera following style is not applied while you are in a saved view. (See: https://us.forums.blizzard.com/en/wow/t/camera-following-style-problembug/442862/17)

==Bugs==

:'''Fixed:''' A bug in 3.0-patches causes SaveView variables not to load first time you load a character after entering the game. 
:::Reloading the UI, or reloading the character from character selection screen, will fix this bug. [http://forums.worldofwarcraft.com/thread.html;jsessionid=232FD6BFB263DD032A2A67227000932E.app25_04?topicId=12454545616&sid=1 Source]
```