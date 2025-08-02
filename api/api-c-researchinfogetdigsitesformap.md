# API C ResearchInfo.GetDigSitesForMap

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ResearchInfo|system=ResearchInfo}}
Returns the dig sites on a map.
 digSites = C_ResearchInfo.GetDigSitesForMap(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;digSites:{{apitype|DigSiteMapInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|researchSiteID}} || {{apitype|number}} || 
|-
| {{apiname|position}} || {{apitype|vector2}} || 
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|poiBlobID}} || {{apitype|number}} || <font color="green">10.2.7</font>
|-
| {{apiname|textureIndex}} || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```