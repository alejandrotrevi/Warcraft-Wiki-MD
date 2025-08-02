# API C CreatureInfo.GetFactionInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the faction name for a race.
 factionInfo = C_CreatureInfo.GetFactionInfo(raceID)

==Arguments==
:;[[RaceId|raceID]]:{{apitype|number}}

==Returns==
:;factionInfo:structure - FactionInfo (nilable)

{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || localized
|-
| groupTag || {{apitype|string}} || locale-independent
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```