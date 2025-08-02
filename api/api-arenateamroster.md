# API ArenaTeamRoster

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Requests the arena team information from the server
 ArenaTeamRoster(index)

==Parameters==
:;index:{{apitype|number}} - Index of the arena team to request information from, 1 through 3.

==Details==
* Because this sends a request to the server, you will not get the data instantly you must register and watch for the <code>ARENA_TEAM_ROSTER_UPDATE</code> event.
* It appears that <code>ARENA_TEAM_ROSTER_UPDATE</code> will not fire if you requested the same team index last call.

==Patch changes==
* {{Patch 5.4.0|note=Removed.}}
```