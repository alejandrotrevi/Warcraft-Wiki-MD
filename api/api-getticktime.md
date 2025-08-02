# API GetTickTime

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the time in seconds since the end of the previous frame and the start of the current frame.

 elapsed = GetTickTime()

==Returns==
:;elapsed:{{apitype|number}} - The time in seconds since the last frame.

==Details==
* Multiple calls to this function within the same frame will all return the same value.
* The value returned from this function appears to be identical to the value passed to [[UIHANDLER_OnUpdate|OnUpdate]] scripts executed at the end of the current frame as the <code>elapsed</code> parameter.

==Patch changes==
* {{Patch 7.0.3|note=Added.<ref>{{ref web|url=https://www.townlong-yak.com/framexml/22267/Util.lua#266|author=Townlong-Yak|date=2016-07-19|title=Util.lua}}</ref>}}

==References==
{{Reflist}}
```