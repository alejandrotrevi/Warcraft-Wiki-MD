# API C MajorFactions.GetMajorFactionRenownInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MajorFactions|system=MajorFactionsUI}}
Needs summary.
 data = C_MajorFactions.GetMajorFactionRenownInfo(majorFactionID)

==Arguments==
:;majorFactionID:{{apitype|number}}

==Returns==
:;data:{{apitype|MajorFactionRenownInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|renownLevel}} || {{apitype|number}} || 
|-
| {{apiname|renownReputationEarned}} || {{apitype|number}} || 
|-
| {{apiname|renownLevelThreshold}} || {{apitype|number}} || 
|}
```