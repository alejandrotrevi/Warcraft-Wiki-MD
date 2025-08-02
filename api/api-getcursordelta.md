# API GetCursorDelta

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the distance that the cursor has moved since the last frame.
 x, y = GetCursorDelta()

==Returns==
:;x:{{apitype|number}} - Distance along the X axis that the cursor has travelled.
:;y:{{apitype|number}} - Distance along the Y axis that the cursor has travelled.

==Details==
* If the cursor hasn't moved between two frames, this function will return zeroes.
* Values returned by this function are independent of UI scaling. The [https://www.townlong-yak.com/framexml/42488/UIParent.lua#4326 GetScaledCursorDelta] utility function can be used to apply the effective scale of UIParent to the returned values.
```