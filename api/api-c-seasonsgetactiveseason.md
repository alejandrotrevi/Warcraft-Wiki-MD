# API C Seasons.GetActiveSeason

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Seasons|system=SeasonsScripts}}
Returns the ID of the season that is active on the current realm.
 seasonID = C_Seasons.GetActiveSeason()

==Returns==
:;seasonID:{{apitype|Enum.SeasonID?}} - The currently active season ID, if one is active.
{{:Enum.SeasonID|nocaption=1}}

==Details==
* Despite the associated SeasonID enumeration having a NoSeason constant defined, this value is presently unused and the function will instead return nil if no season is active.

==Patch changes==
<!-- Below change is an estimation; it was first noticed ~July 2024 however it may be older. -->
* {{Patch 1.15.3|note=This function now returns nil instead of the NoSeason constant if no season is active.}}
* {{Patch 1.14.1|note=Added.}}

{{apinavbox|Authoring}}
```