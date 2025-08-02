# API DeathRecap GetEvents

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a table representing the last five damaging combat events against the player.
 events = DeathRecap_GetEvents([recapID])

==Arguments==
:;recapID:{{apitype|number}} - The specific death to view, from 1 to the most recent death. If this is not given, the most recent ID is used.

==Returns==
:;events:{{apitype|table}} - A table of events for the chosen death, or nil if the player has not died this session.

==Details==
The return table contains five sub tables. The keys for these tables are the same as the param names used for [[COMBAT_LOG_EVENT]].

Example:
 [1]={
     [1]={
         timestamp=1421121447.489,
         event="SWING_DAMAGE",
         hideCaster=false,
         sourceGUID="Creature-0-3296-870-59-72280-0000347644",
         sourceName="Manifestation of Pride",
         sourceFlags=2632,
         sourceRaidFlags=0,
         destGUID="Player-3296-0084A447"
         destName="Gethe",
         destFlags=1297,
         destRaidFlags=0,
         amount=1472,
         overkill=-1,
         school=1,
         critical=false,
         glancing=false,
         crushing=false,
         isOffHand=false,
         multistrike=false,
         currentHP=2185,
     },
     [2]={...},
     [3]={...},
     [4]={...},
     [5]={...},
 }
 
==Patch changes==
* {{Patch 6.1.0|note=Added}}

==See also==
* {{api|DeathRecap_HasEvents}}
* {{api|GetDeathRecapLink}}
```