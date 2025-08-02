# API C GossipInfo.GetGossipPoiForUiMapID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the id of a gossip point of interest, a temporary marker most often appearing after asking city guards for directions.
 gossipPoiID = C_GossipInfo.GetGossipPoiForUiMapID(uiMapID)

==Arguments==
:;[[UiMapID|uiMapID]]:{{apitype|number}}

==Returns==
:;gossipPoiID:{{apitype|number?}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}

==See also==
* {{api|C_GossipInfo.GetGossipPoiInfo}} - to obtain further information about the point of interest using the gossipPoiID as an argument
* {{api|DYNAMIC_GOSSIP_POI_UPDATED|t=e}} - Indicator that '''GetGossipPoiForUiMapID''' may now return a different value than before
```