# API C MajorFactions.GetMajorFactionData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MajorFactions|system=MajorFactionsUI}}
Needs summary.
 data = C_MajorFactions.GetMajorFactionData(majorFactionID)

==Arguments==
:;majorFactionID:{{apitype|number}}

==Returns==
:;data:{{apitype|MajorFactionData?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| factionID || {{apitype|number}} || 
|-
| expansionID || {{apitype|number}} || 
|-
| bountySetID || {{apitype|number}} || 
|-
| isUnlocked || {{apitype|boolean}} || 
|-
| unlockDescription || {{apitype|string?}} || 
|-
| unlockOrder || {{apitype|number}} || 
|-
| renownLevel || {{apitype|number}} || 
|-
| renownReputationEarned || {{apitype|number}} || 
|-
| renownLevelThreshold || {{apitype|number}} || 
|-
| textureKit || {{apitype|string}} || 
|-
| celebrationSoundKit || {{apitype|number}} || 
|-
| renownFanfareSoundKitID || {{apitype|number}} || 
|}
```