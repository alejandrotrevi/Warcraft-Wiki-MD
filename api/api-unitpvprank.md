# API UnitPVPRank

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the specified unit's PvP rank ID.
 rankID = UnitPVPRank(unit)

==Arguments==
:;[[unit]]:{{apitype|string}}

==Returns==
:;rankID:{{apitype|number}} - Starts at 5 (not at 1) for the first rank. Returns 0 if the unit has no rank. Can be used in {{api|GetPVPRankInfo}}() for rank information.

==Example==
 local rankID = UnitPVPRank("target")
 local rankName, rankNumber = GetPVPRankInfo(rankID)
 if rankName then
 	print(format("%s is rank ID %d, rank number %d (%s)", UnitName("target"), rankID, rankNumber, rankName))
 end

 > Koribli is rank ID 12, rank number 8 (Knight-Captain)

==Values==
{{:API_GetPVPRankInfo}}

==Patch changes==
* {{Patch 5.4.0|note=Removed.}}
* {{Patch 1.4.0|note=Added.}}
```