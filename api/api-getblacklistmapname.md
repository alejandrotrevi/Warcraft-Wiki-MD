# API GetBlacklistMapName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns name of a blacklisted PvP map.
 mapName = GetBlacklistMapName(index)

==Arguments==
:;index:{{apitype|number}} - map blacklist index, ascending from 1.

==Returns==
:;mapName:{{apitype|string}} - name of the blacklisted PvP map (e.g. "Warsong Gulch"), nil if none.

==Patch changes==
* {{Patch 5.2.0|note=Added.}}

==See also==
* {{api|GetBlacklistMap}}
```