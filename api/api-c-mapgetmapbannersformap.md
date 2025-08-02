# API C Map.GetMapBannersForMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns the poi banners for a map.
 mapBanners = C_Map.GetMapBannersForMap(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;mapBanners:{{apitype|MapBannerInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| areaPoiID || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| atlasName || {{apitype|string}} || 
|-
| uiTextureKit || {{apitype|string?}} || 
|}

==Patch changes==
* {{Patch 8.1.0|note=Added <code>uiTextureKit</code> field.}}
* {{Patch 8.0.1|note=Added.}}
```