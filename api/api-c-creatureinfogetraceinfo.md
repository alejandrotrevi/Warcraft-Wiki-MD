# API C CreatureInfo.GetRaceInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns both localized and locale-independent race names.
 raceInfo = C_CreatureInfo.GetRaceInfo(raceID)

==Arguments==
:;[[RaceId|raceID]]:{{apitype|number}}

==Returns==
:;raceInfo:structure - RaceInfo (nilable)

{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| raceName || {{apitype|string}} || localized name, e.g. "Night Elf"
|-
| clientFileString || {{apitype|string}} || non-localized name, e.g. "NightElf"
|-
| raceID || {{apitype|number}} ||
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```