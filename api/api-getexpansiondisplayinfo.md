# API GetExpansionDisplayInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Expansion}}
Returns the logo and banner textures for an expansion id.
 info = GetExpansionDisplayInfo(expansionLevel)

==Arguments==
:;expansionLevel:{{apitype|number}}
{{:LE_EXPANSION}}

==Returns==
:;info:{{apitype|ExpansionDisplayInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|logo}} || {{apitype|fileID}} || 
|-
| {{apiname|banner}} || {{apitype|textureAtlas}} || 
|-
| {{apiname|features}} || {{apitype|ExpansionDisplayInfoFeature[]}} || 
|-
| {{apiname|highResBackgroundID}} || {{apitype|fileID}} || <font color="green">10.0.0</font>
|-
| {{apiname|lowResBackgroundID}} || {{apitype|fileID}} || <font color="green">10.0.0</font>
|-
| {{apiname|textureKit}} || {{apitype|textureKit}} || <font color="green">11.2.0</font>
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ ExpansionDisplayInfoFeature
! Field !! Type !! Description
|-
| {{apiname|icon}} || {{apitype|fileID}} || 
|-
| {{apiname|text}} || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 7.3.2|note=Added.}}
```