# API C GossipInfo.GetPoiForUiMapID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Returns any gossip point of interest on the map.
 gossipPoiID = C_GossipInfo.GetPoiForUiMapID(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;gossipPoiID:{{apitype|number?}}

==Patch changes==
* {{Patch 9.0.1|note=Changed to <code>C_GossipInfo.GetPoiForUiMapID()</code>}}
* {{Patch 8.0.1|note=Added as {{api|C_GossipInfo.GetGossipPoiForUiMapID}}()}}
```