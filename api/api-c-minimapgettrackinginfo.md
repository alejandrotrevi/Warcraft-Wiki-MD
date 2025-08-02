# API C Minimap.GetTrackingInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Minimap|system=Minimap}}
Needs summary.
 trackingInfo = C_Minimap.GetTrackingInfo(spellIndex)

==Arguments==
:;spellIndex:{{apitype|number}}

==Returns==
:;trackingInfo:{{apitype|MinimapScriptTrackingInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|texture}} || {{apitype|fileID}} || 
|-
| {{apiname|active}} || {{apitype|boolean}} || 
|-
| {{apiname|type}} || {{apitype|string}} || 
|-
| {{apiname|subType}} || {{apitype|number}} || 
|-
| {{apiname|spellID}} || {{apitype|number?}} || 
|}

==Patch changes==
* {{Patch 11.0.0|note=Returns a structured table.|comment=The old signature was <code>name, textureFileID, active, type, subType, spellID = C_Minimap.GetTrackingInfo(spellIndex)</code>}}
```