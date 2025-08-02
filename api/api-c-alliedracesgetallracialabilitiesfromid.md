# API C AlliedRaces.GetAllRacialAbilitiesFromID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the racial spells from an allied race.
 allDisplayInfo = C_AlliedRaces.GetAllRacialAbilitiesFromID(raceID)

==Arguments==
:;[[RaceId|raceID]]:{{apitype|number}}

==Returns==
:;allDisplayInfo:structure - AlliedRaceRacialAbility[]

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| description || string ||
|-
| name || string ||
|-
| icon || number ||
|}

==Patch changes==
* {{Patch 7.3.5|note=Added.}}
```