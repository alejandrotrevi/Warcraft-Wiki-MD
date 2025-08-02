# API GetFramerate

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current framerate.
 framerate = GetFramerate()

==Returns==
:;framerate:{{apitype|number}} - The current framerate in frames per second.

==Example==
<syntaxhighlight lang="lua">
local framerate = GetFramerate()
print("Your current framerate is "..floor(framerate).." fps")
</syntaxhighlight>

==Details==
* Notice the returned value adjusts slowly when the FPS quickly drops from 60 to 6, for example. If the FPS drops very fast, this function will be decreasing to 40, 20, 15, etc, for the next couple seconds until it reaches 6. This delay means it is not as accurate as third party FPS programs, but still functional. Alternatively, no delay is seen when the FPS is increased quickly.

* You can also toggle the Framerate Display with [https://www.townlong-yak.com/framexml/go/ToggleFramerate ToggleFramerate] (normally the <code>Ctrl-R</code> hotkey). You can also see the same framerate in the tooltip of the GameMenu button on the main actionbar.

[[File:API_GetFramerate_01.png|link=]]
```