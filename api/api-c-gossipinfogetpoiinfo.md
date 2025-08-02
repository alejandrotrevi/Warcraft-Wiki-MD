# API C GossipInfo.GetPoiInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Returns info for a gossip point of interest (e.g. the red flags when asking city guards for directions).
 gossipPoiInfo = C_GossipInfo.GetPoiInfo(uiMapID, gossipPoiID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]
:;gossipPoiID:{{apitype|number}}

==Returns==
:;gossipPoiInfo:{{apitype|GossipPoiInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| textureIndex || {{apitype|number}} || Used for {{api|GetPOITextureCoords}}()
|-
| position || {{apitype|Vector2DMixin}} || 
|-
| inBattleMap || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_GossipInfo.GetPoiInfo()</code>}}
* {{Patch 8.0.1|note=Added as <code>C_GossipInfo.GetGossipPoiInfo()</code>}}
```