# API GetPVPTimer

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the time left in milliseconds until the player is unflagged for PvP.
 timer = GetPVPTimer()

==Returns==
:;timer:{{apitype|number}} - Amount of time (in milliseconds) until your PVP flag wears off.

==Details==
* If you are flagged for PVP permanently, the function returns 301000.
* If you are not flagged for PVP the function returns either 301000 or -1.

==Example==
The following snippet displays your current PVP status:
 local sec = math.floor(GetPVPTimer()/1000)
 local msg = (not UnitIsPVP("player")) and "You are not flagged for PVP" or 
             (sec==301 and "You are perma-flagged for PVP" or 
              "Your PVP flag wears off in "..(sec>60 and math.floor(sec/60).." minutes " or "")..(sec%60).." seconds")
 DEFAULT_CHAT_FRAME:AddMessage(msg)
```