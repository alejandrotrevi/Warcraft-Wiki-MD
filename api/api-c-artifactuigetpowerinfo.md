# API C ArtifactUI.GetPowerInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 powerInfo = C_ArtifactUI.GetPowerInfo(powerID)

==Arguments==
:;powerID:{{apitype|number}}

==Returns==
:;powerInfo:structure - ArtifactPowerInfo

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| spellID || {{apitype|number}} ||
|-
| cost || {{apitype|number}} ||
|-
| currentRank || {{apitype|number}} ||
|-
| maxRank || {{apitype|number}} ||
|-
| bonusRanks || {{apitype|number}} ||
|-
| numMaxRankBonusFromTier || {{apitype|number}} ||
|-
| prereqsMet || {{apitype|boolean}} ||
|-
| isStart || {{apitype|boolean}} ||
|-
| isGoldMedal || {{apitype|boolean}} ||
|-
| isFinal || {{apitype|boolean}} ||
|-
| tier || {{apitype|number}} ||
|-
| position || {{apitype|Vector2DMixin}} || 
|-
| offset || {{apitype|Vector2DMixin?}} || 
|-
| linearIndex || {{apitype|number?}} ||
|}

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```