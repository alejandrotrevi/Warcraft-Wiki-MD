# API GetPVPLastWeekStats

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the player's PVP contribution statistics for the previous week.
 hk, dk, contribution, rank = GetPVPLastWeekStats()

==Returns==
:;hk:{{apitype|number}} - The number of honorable kills.
:;dk:{{apitype|number}} - The number of dishonorable kills.
:;contribution:{{apitype|number}} - The estimated number of honor contribution points.
:;rank:{{apitype|number}} - The honor rank the player had.

==Patch changes==
* {{Patch 2.0.1|note=Removed.}}
* {{Patch 1.4.0|note=Added.}}
```