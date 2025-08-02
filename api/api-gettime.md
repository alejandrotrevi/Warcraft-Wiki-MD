# API GetTime

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the system uptime of your computer in seconds, with millisecond precision.
 seconds = GetTime()

==Returns==
:;seconds:{{apitype|number}} - The current system uptime in seconds, e.g. 60123.558

==Details==
* This value is only updated once per rendered frame. Finer-grained timers are available using {{api|GetTimePreciseSec}}() or {{api|debugprofilestop}}().
* It is possible for this function to return identical values across consecutive frames if a low resolution [[CVar timingMethod|timing method]] is in use while running at a high framerate.

==Patch changes==
* {{Patch 4.3.0|note=Only updates once every OnUpdate<sup>[http://www.wowinterface.com/forums/showthread.php?t=41919#6]</sup>}}

==See also==
* {{api|time}}(), {{api|date}}()
* {{api|GetGameTime}}()
* {{api|GetTimePreciseSec}}()
* [[CVar timingMethod]]
```