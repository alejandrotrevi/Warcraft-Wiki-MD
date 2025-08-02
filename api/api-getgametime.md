# API GetGameTime

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the realm's current time in hours and minutes.
 hours, minutes = GetGameTime()

==Returns==
:;hours:{{apitype|number}} - The current hour (0-23).
:;minutes:{{apitype|number}} - The minutes passed in the current hour (0-59).

==Details==
* This function can unexpectedly return results inconsistent with actual realm server time.  The value returned is from the physical [[instance]] server you are actually playing on, and not that of the world instance server (realm server) you log into. Servers for instances such as for raids and PvP are often shared between login world servers, and instance servers are not always running using the same timezone as the login realm server. This is particularly noticeable for Oceanic and other low population world servers.

==Example==
<syntaxhighlight lang="lua">
/dump GetGameTime() -- 18, 41
</syntaxhighlight>

==Comparison==
{{:API_GetServerTime}}

==See also==
* {{api|time}}()
* {{api|GetTime}}()
```