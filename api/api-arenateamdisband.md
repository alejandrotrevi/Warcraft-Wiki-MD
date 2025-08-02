# API ArenaTeamDisband

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Disbands an Arena Team if the player is the team captain.
 ArenaTeamDisband(index)

==Arguments==
:;index:{{apitype|number}} - Index of the arena team to delete, index can be a value of 1 through 3.

==Example==
The following macro disbands the first arena team.
 /run ArenaTeamDisband(1)

It can be used as the last solution to get rid of an arena team if all the other members of it don't come online anymore or if you just want to delete it. So far there is no UI implementation of this.

==Patch changes==
* {{Patch 5.4.0|note=Removed.}}
```