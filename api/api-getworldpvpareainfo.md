# API GetWorldPVPAreaInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns info for a world PvP zone (e.g. Wintergrasp or Tol Barad).

 pvpID, localizedName, isActive, canQueue, startTime, canEnter, minLevel, maxLevel = GetWorldPVPAreaInfo(index)

==Arguments==
:;index:{{apitype|number}} - the zone's index, from 1 to {{api|GetNumWorldPVPAreas}}()
:: 1 - Wintergrasp
:: 2 - Tol Barad
:: 3 - Ashran

==Returns==
:pvpID, localizedName, isActive, canQueue, startTime, canEnter, minLevel, maxLevel

:;pvpID:{{apitype|number}} - the PvP queue ID for the specified world PvP area
:;localizedName:{{apitype|string}} - the zone's name, in the current locale
:;isActive:{{apitype|boolean}} - whether a battle is currently taking place in the zone
:;canQueue:{{apitype|boolean}} - whether players can currently queue for the next or current battle
:;startTime:{{apitype|number}} - time until the next battle starts, in seconds
:;canEnter:{{apitype|boolean}} - whether the player meets the necessary requirements to participate in the zone's battle
:;minLevel:{{apitype|number}} - minimum character level required to join the battle
:;maxLevel:{{apitype|number}} - maximum character level allowed

==Example==
 local _, localizedName, _, canQueue, startTime, canEnter = GetWorldPVPAreaInfo(2)
 
 if startTime > 0 then
     print("Cool your jets, " .. localizedName .. " doesn't start for another " .. SecondsToTime(startTime) .. ".")
 elif canEnter and canQueue then
     print("Get over to " .. localizedName .. ", quick!")
 else
     print("They're fighting over in " .. localizedName .. ".  Don't you wish you could join in?")
 end

<big>'''Result'''</big>
 -- if the battle hasn't started yet
 "Cool your jets, Tol Barad doesn't start for another 12:34."

 -- if the battle is active and the player can join it
 "Get over to Tol Barad, quick!"

 -- if the battle is active but the player cannot join
 "They're fighting over in Tol Barad.  Don't you wish you could join in?"

==Details==
: Note that there is some redundancy in the return values.  For example, isActive will always be false when startTime is greater than 0.
```