# API UnitRace

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the race of the unit.
 localizedRaceName, englishRaceName, raceID = UnitRace(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;localizedRaceName:{{apitype|string}} - Localized race name, suitable for use in user interfaces.
:;englishRaceName:{{apitype|string}} - Localization-independent race name, suitable for use as table keys.
:;raceID:{{apitype|number}} - [[RaceId]]. Localization-independent raceID.

==Example==
The following command prints your character's name and race to chat:
 /run print(UnitName("player").." is a "..UnitRace("player"))

==Values==
{{:RaceId}}

==Patch changes==
* {{Patch 8.2.0|note=Can now return Mechagnome.}}
* {{Patch 5.0.4|note=Can now return Pandaren.}}
* {{Patch 4.0.1|note=Can now return Goblin, Worgen.}}
* {{Patch 2.0.1|note=Can now return Blood Elf, Draenei.}}

==See also==
* {{api|UnitClass}}()
* {{api|C_CreatureInfo.GetRaceInfo}}()
```