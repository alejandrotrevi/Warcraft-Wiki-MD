# API C MajorFactions.GetRenownLevels

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MajorFactions|system=MajorFactionsUI}}
Needs summary.
 levels = C_MajorFactions.GetRenownLevels(majorFactionID)

==Arguments==
:;majorFactionID:{{apitype|number}}

==Returns==
:;levels:{{apitype|MajorFactionRenownLevelInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| factionID || {{apitype|number}} || 
|-
| level || {{apitype|number}} || 
|-
| locked || {{apitype|boolean}} || 
|-
| isMilestone || {{apitype|boolean}} || 
|-
| isCapstone || {{apitype|boolean}} || 
|}
```