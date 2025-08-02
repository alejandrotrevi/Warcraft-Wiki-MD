# API C AlliedRaces.GetRaceInfoByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AlliedRaces|system=AlliedRaces}}
Returns allied race info.
 info = C_AlliedRaces.GetRaceInfoByID(raceID)

==Arguments==
:;raceID:{{apitype|number}} : [[RaceId]]

==Returns==
:;info:{{apitype|AlliedRaceInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| raceID || {{apitype|number}} || 
|-
| maleModelID || {{apitype|number}} || 
|-
| femaleModelID || {{apitype|number}} || 
|-
| achievementIds || {{apitype|number[]}} || 
|-
| maleName || {{apitype|string}} || 
|-
| femaleName || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| raceFileString || {{apitype|string}} || 
|-
| crestAtlas || {{apitype|textureAtlas}} || 
|-
| modelBackgroundAtlas || {{apitype|textureAtlas}} || 
|-
| bannerColor || {{apitype|colorRGB}} || 
|}

==Patch changes==
* {{Patch 9.0.2|note=Added <code>achievementIds</code> field.}}
* {{Patch 8.1.0|note=Added <code>maleName, femaleName</code> fields.}}
* {{Patch 7.3.5|note=Added.}}
```