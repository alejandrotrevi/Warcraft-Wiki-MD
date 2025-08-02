# API C MythicPlus.GetCurrentSeason

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current Mythic Plus season.
 seasonID = C_MythicPlus.GetCurrentSeason()

==Returns==
:;seasonID:{{apitype|number}}

== Details ==
Returns the current Mythic Plus season. Returns -1 until {{api|C_MythicPlus.RequestMapInfo}}() is called at least once.

Returns 0 when there is no active season. (To be confirmed)

== Seasons ==
{| class="fandom-table"
|+
!Season Id
!Name
|-
|1
|Battle for Azeroth Season 1
|-
|2
|Battle for Azeroth Season 2
|-
|3
|Battle for Azeroth Season 3
|-
|4
|Battle for Azeroth Season 4
|-
|5
|Shadowlands Season 1
|-
|6
|Shadowlands Season 2
|-
|7
|Shadowlands Season 3
|-
|8
|Shadowlands Season 4
|-
|9
|Dragonflight Season 1
|-
|10
|Dragonflight Season 2
|-
|11
|Dragonflight Season 3
|-
|12
|Dragonflight Season 4
|-
|13
|The War Within Season 1
|-
|14
|The War Within Season 2
|-
|15
|The War Within Season 3 - unconfirmed
|-
|16
|The War Within Season 4 - unconfirmed
|}

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```