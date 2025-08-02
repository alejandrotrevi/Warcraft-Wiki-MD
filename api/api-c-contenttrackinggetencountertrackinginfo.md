# API C ContentTracking.GetEncounterTrackingInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ContentTracking|system=ContentTracking}}
Needs summary.
 trackingInfo = C_ContentTracking.GetEncounterTrackingInfo(journalEncounterID)

==Arguments==
:;journalEncounterID:{{apitype|number}}

==Returns==
:;trackingInfo:{{apitype|EncounterTrackingInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| encounterName || {{apitype|string}} || 
|-
| journalEncounterID || {{apitype|number?}} || 
|-
| journalInstanceID || {{apitype|number?}} || 
|-
| instanceName || {{apitype|string}} || 
|-
| subText || {{apitype|string?}} || 
|-
| difficultyID || {{apitype|number?}} || 
|-
| lfgDungeonID || {{apitype|number?}} || 
|-
| groupFinderActivityID || {{apitype|number?}} || 
|}
```