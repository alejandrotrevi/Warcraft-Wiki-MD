# API C InvasionInfo.GetInvasionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns invasion info.
 invasionInfo = C_InvasionInfo.GetInvasionInfo(invasionID)

==Arguments==
:;{{dbc|invasionclientdata|invasionID}}:number

==Returns==
:;invasionInfo:structure - InvasionMapInfo

{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| invasionID || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| position || {{apitype|Vector2DMixin}} || 
|-
| atlasName || {{apitype|string}} || [[AtlasID]]
|-
| rewardQuestID || {{apitype|number?}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```