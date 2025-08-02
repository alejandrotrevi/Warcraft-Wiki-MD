# API C FogOfWar.GetFogOfWarInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_FogOfWar|system=FogOfWar}}
Returns info for the fog of war for an [[Island Expedition]] map.
 fogOfWarInfo = C_FogOfWar.GetFogOfWarInfo(fogOfWarID)

==Arguments==
:;fogOfWarID:{{apitype|number}} : {{dbc|uimapfogofwar|UiMapFogOfWar.db2}}

==Returns==
:;fogOfWarInfo:{{apitype|FogOfWarInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
<!-- |+ [[Struct FogOfWar.FogOfWarInfo|FogOfWarInfo]] -->
! Field !! Type !! Description
|-
| fogOfWarID || {{apitype|number}} ||
|-
| backgroundAtlas || {{apitype|string}} ||
|-
| maskAtlas || {{apitype|string}} ||
|-
| maskScalar || {{apitype|number}} ||
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```