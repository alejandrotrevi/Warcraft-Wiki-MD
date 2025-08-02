# API GetZonePVPInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|note=''This function was deprecated in patch <font color=#ecbc2a>10.2.6</font> and might be removed in patch <font color=#ecbc2a>11.0.2</font> or later.''}}
Returns PVP info for the current zone.
 pvpType, isFFA, faction = GetZonePVPInfo()

==Returns==
:;pvpType:{{apitype|string}} - One of the following values:
:*"arena" if you are in an arena
:*"friendly" if the zone is controlled by the faction the player belongs to.
:*"contested" if the zone is contested (PvP server only)
:*"hostile" if the zone is controlled by the opposing faction.
:*"sanctuary" if the zone is a sanctuary and does not allow pvp combat (2.0.x).
:*"combat" if it is a combat zone where players are automatically flagged for PvP combat (3.0.x). Currently applies only to the [[Wintergrasp]] zone.
:*nil, if the zone is none of the above. Happens inside instances, ''including battlegrounds'', and on PvE servers when the zone would otherwise be "contested".
:;isFFA:{{apitype|boolean}} - true if in a free-for-all arena.
:;faction:{{apitype|string}} - the name of the faction controlling the zone if pvpType is "friendly" or "hostile".

==Example==
 local zone = GetRealZoneText().." - "..tostring(GetSubZoneText())
 local pvpType, isFFA, faction = GetZonePVPInfo()
 local str
 if pvpType =="friendly" or pvpType== "hostile" then
 	str = " is controlled by "..faction.." ("..pvpType..")"
 elseif pvpType == "sanctuary" then
 	str = " is a PvP-free sanctuary."
 elseif isFFA then
 	str = " is a free-for-all arena."
 else
 	str = " is a contested zone."
 end
 print(zone..str)

 Stormwind City - War Room is controlled by Alliance (friendly)
 Alterac Valley - Dun Baldar Pass is a contested zone.
```