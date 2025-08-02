# API GetPlayerInfoByGUID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns character info for another player from their GUID.
 localizedClass, englishClass, localizedRace, englishRace, sex, name, realmName = GetPlayerInfoByGUID(guid)

==Arguments==
:;guid:{{apitype|string}} - The [[GUID]] of the player you're querying.

==Returns==
:;localizedClass:{{apitype|string}} - Localized class name.
:;englishClass:{{apitype|string}} - Localization-independent [[ClassId|class name]].
:;localizedRace:{{apitype|string}} - Localized race name.
:;englishRace:{{apitype|string}} - Localization-independent [[RaceId|race name]].
:;sex:{{apitype|number}} - [[API_UnitSex|Gender ID]] of the character. 2 for male, or 3 for female.
:;name:{{apitype|string}} - The name of the character.
:;realmName:{{apitype|string}} - [[API GetRealmName|Normalized]] realm name of the character. Returns an empty string if the character is from the same realm as the player.

==Example==
* When used on yourself.
 /dump UnitGUID("target"), GetPlayerInfoByGUID(UnitGUID("target"))
<syntaxhighlight lang="lua">
> "Player-1096-06DF65C1", "Priest", "PRIEST", "Human", "Human", 3, "Xiaohuli", ""
</syntaxhighlight>

* When used on a player from another realm, in this case from the same connected realm.
<syntaxhighlight lang="lua">
> "Player-1096-0971D0BE", "Monk", "MONK", "Night Elf", "NightElf", 2, "Coldbits", "DarkmoonFaire"
</syntaxhighlight>

==Details==
* Players with hexadecimal characters or a <code>!</code> appending their name are flagged for a name change.

==Patch changes==
* {{Patch 3.2.0|note=Added.}}
```