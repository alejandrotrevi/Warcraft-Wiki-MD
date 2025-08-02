# API GetBlacklistMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the battleground map ID of a blacklisted PvP map.
 bgMapID = GetBlacklistMap(index)

==Arguments==
:;index:{{apitype|number}} - map blacklist index, ascending from 1.

==Returns==
:;bgMapID:Numer - battleground map ID of the blacklisted map; -1 if none.

==Details==
* <code>bgMapID</code> corresponds to the values returned from {{api|GetBattlegroundInfo}}.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|GetBlacklistMapName}}
```