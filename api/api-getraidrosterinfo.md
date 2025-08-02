# API GetRaidRosterInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a member of your raid.
 name, rank, subgroup, level, class, fileName, zone, online, isDead, role, isML, combatRole = GetRaidRosterInfo(raidIndex)

==Arguments==
:;raidIndex:{{apitype|number}} - The [[raidIndex|index]] of a raid member between 1 and <code>MAX_RAID_MEMBERS</code> (40). It's discouraged to use {{api|GetNumGroupMembers}}() since there can be "holes" between raid1 to raid40.

==Returns==
:;name:{{apitype|string}} - raid member's name. Returns "Name-Server" for cross-realm players.
:;rank:{{apitype|number}} - Returns 2 if the raid member is the leader of the raid, 1 if the raid member is promoted to assistant, and 0 otherwise.
:;subgroup:{{apitype|number}} - The raid party this character is currently a member of.  Raid subgroups are numbered as on the standard raid window.
:;level:{{apitype|number}} - The level of the character.  If this character is offline, the level will show as 0 (not nil).
:;class:{{apitype|string}} - The character's class (localized), with the first letter capitalized (e.g. "Priest"). This function works as normal for offline characters.
:;fileName:{{apitype|string}} - The system representation of the character's class; always in english, always fully capitalized.
:;zone:{{apitype|string?}} - The name of the zone this character is currently in.  This is the value returned by [[API GetRealZoneText|GetRealZoneText]].  It is the same value you see if you mouseover their portrait (if in group).  If the character is offline, this value will be the string "Offline".
:;online:{{apitype|boolean}} - Returns 1 if raid member is online, nil otherwise.
:;isDead:{{apitype|boolean}} - Returns 1 if raid member is dead (hunters Feigning Death are considered alive), nil otherwise.
:;role:{{apitype|string}} - The player's role within the raid ("maintank" or "mainassist").
:;isML:{{apitype|boolean}} - Returns 1 if the raid member is master looter, nil otherwise
:;combatRole:{{apitype|string}} - Returns the combat role of the player if one is selected, i.e. "DAMAGER", "TANK" or "HEALER". Returns "NONE" otherwise.

==Details==
* Do not make any assumptions about raidid (raid1, raid2, etc) to name mappings remaining the same or not. When the raid changes, people MAY retain it or not, depending on raid size and WoW patch. Yes, this behavior has changed with patches in the past and may do it again.
* ''zone'' can return nil for oneself (unitId == "player") if one has not changed locations since last reloading the UI.  After changing locations, this returns.  Use {{api|PlayerLocation CreateFromUnit("player")|PlayerLocation:CreateFromUnit}} as a workaround.
* When an out of bounds index is used (more than the players in a raid, or beyond MAX_RAID_MEMBERS), some non-nil return values are possible: <syntaxhighlight lang="lua" inline="true">[2]=0, [3]=1, [4]=1, [11]=false, [12]="NONE"</syntaxhighlight>.
```