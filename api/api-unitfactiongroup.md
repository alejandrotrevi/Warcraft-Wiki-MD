# API UnitFactionGroup

**Contributor:** Plusmouse

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the faction (Horde/Alliance) a unit belongs to.
 englishFaction, localizedFaction = UnitFactionGroup(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;englishFaction:{{apitype|string}} - Unit's faction name in English, i.e. "Alliance", "Horde", "Neutral" or nil.
:;localizedFaction:{{apitype|string}} - Unit's faction name in the client's locale or nil.

==Details==
* The function returns may not return correct results until after PLAYER_ENTERING_WORLD event for units other than "player".
* Note that for NPCs, the function will only return Alliance/Horde for factions closely allied with either side. Goblins, for instance, return <code>nil,nil</code>.
* Pandaren player characters on the [[Wandering Isle]] return "Neutral", "".
```