# API C ContributionCollector.GetContributionCollectorsForMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns contribution buildings on a map.
 contributionCollectors = C_ContributionCollector.GetContributionCollectorsForMap(uiMapID)

==Arguments==
:;[[UiMapID|uiMapID]]:{{apitype|number}}

==Returns==
:;contributionCollectors:structure - ContributionMapInfo[]

{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| areaPoiID || {{apitype|number}} || 
|-
| position || {{apitype|Vector2DMixin}} || 
|-
| name || {{apitype|string}} || 
|-
| atlasName || {{apitype|string}} || 
|-
| collectorCreatureID || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```