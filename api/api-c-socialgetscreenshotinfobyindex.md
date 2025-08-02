# API C Social.GetScreenshotInfoByIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the display resolution of a screenshot.
 screenWidth, screenHeight = C_Social.GetScreenshotInfoByIndex(index)

==Arguments==
:;index:{{apitype|number}} - index of the screenshot. Does not persist between sessions.

==Returns==
:;screenWidth:{{apitype|number}} - width of the screen in pixels.
:;screenHeight:{{apitype|number}} - height of the screen in pixels.

==Example==
Prints the screenshot information of this session.
 for i = 1, C_Social.GetLastScreenshotIndex() do
 	local width, height = C_Social.GetScreenshotInfoByIndex(i)
 	print(i, width, height)
 end

==Patch changes==
* {{Patch 8.1.5|note=Moved to {{api|C_Social.GetScreenshotInfoByIndex}}. The previous alias is deprecated. [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_5.lua#38]}}
* {{Patch 6.1.0|note=Added as {{api|C_Social.GetScreenshotByIndex}}.}}
```