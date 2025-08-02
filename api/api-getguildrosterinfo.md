# API GetGuildRosterInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a guild member.
 name, rankName, rankIndex, level, classDisplayName, zone, publicNote, officerNote, isOnline, status, class, achievementPoints, achievementRank, isMobile, canSoR, repStanding, guid = GetGuildRosterInfo(index)

==Arguments==
:;index:{{apitype|number}} - Ranging from 1 to {{api|GetNumGuildMembers}}()

==Returns==
:;name:{{apitype|string}} - Name of character with realm (e.g. "Arthas-Silvermoon")
:;rankName:{{apitype|string}} - Name of character's guild rank (e.g. Guild Master, Officer, Member, ...)
:;rankIndex:{{apitype|number}} - Index of rank starting at 0 for GM (add 1 for [[API GuildControlGetRankName|GuildControlGetRankName(index)]])
:;level:{{apitype|number}} - Character's level
:;classDisplayName:{{apitype|string}} - Localized class name (e.g. "Mage", "Warrior", "Guerrier", ...)
:;zone:{{apitype|string}} - Character's location (last location if offline)
:;publicNote:{{apitype|string}} - Character's public note, returns "" if you can't view notes or no note
:;officerNote:{{apitype|string}} - Character's officer note, returns "" if you can't view notes or no note
:;isOnline:{{apitype|boolean}} - true: online - false: offline
:;status:{{apitype|number}} - 0: none - 1: AFK - 2: Busy (Do Not Disturb) (changed in 4.3.2)
:;class:{{apitype|string}} - Localization-independent class name (e.g. "MAGE", "WARRIOR", "DEATHKNIGHT", ...)
:;achievementPoints:{{apitype|number}} - Character's [[achievement|achievement points]]
:;achievementRank:{{apitype|number}} - Where the character ranks in guild if sorted by achievement points
:;isMobile:{{apitype|boolean}} - true: player logged into app with this character
:;canSoR:{{apitype|boolean}} - true: can use [[Scroll of Resurrection]] on character (deprecated)
:;repStanding:{{apitype|number}} - [[StandingId|Standing ID]] for character's [[guild reputation]]
:;guid:{{apitype|string}} - Character's [[GUID]]

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|C_GuildInfo.GuildRoster}} }}
{{apirow | Related Events | {{api|t=e|GUILD_ROSTER_UPDATE}} }}
|}
```