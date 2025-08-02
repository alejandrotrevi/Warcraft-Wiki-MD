# API C Texture.GetAtlasInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Texture|system=TextureUtils}}
Returns atlas info.
 info = C_Texture.GetAtlasInfo(atlas)

==Arguments==
:;atlas:{{apitype|string}} - Name of the [[atlasID|atlas]]

==Returns==
[[File:API_C_Texture.GetAtlasInfo.png|frame|right|[https://wago.tools/db2/UiTextureAtlasMember?filter%5BCommittedName%5D=MainPet-PetFamilyFrame MainPet-PetFamilyFrame], part of FileID [https://wago.tools/files?search=878877 878877] ]]
:;info:{{apitype|AtlasInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|elementName}} || {{apitype|string}} || <font color="green">11.1.5</font>
|-
| {{apiname|width}} || {{apitype|number}} || 
|-
| {{apiname|height}} || {{apitype|number}} || 
|-
| {{apiname|rawSize}} || {{apitype|vector2}} || <font color="green">10.2.0</font>
|-
| {{apiname|leftTexCoord}} || {{apitype|number}} || 
|-
| {{apiname|rightTexCoord}} || {{apitype|number}} || 
|-
| {{apiname|topTexCoord}} || {{apitype|number}} || 
|-
| {{apiname|bottomTexCoord}} || {{apitype|number}} || 
|-
| {{apiname|tilesHorizontally}} || {{apitype|boolean}} || 
|-
| {{apiname|tilesVertically}} || {{apitype|boolean}} || 
|-
| {{apiname|file}} || {{apitype|fileID?}} || FileID of parent texture
|-
| {{apiname|filename}} || {{apitype|string?}} || 
|-
| {{apiname|sliceData}} || {{apitype|UITextureSliceData?}} || <font color="green">10.2.0</font>
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ UITextureSliceData
! Field !! Type !! Description
|-
| {{apiname|marginLeft}} || {{apitype|number}} || 
|-
| {{apiname|marginTop}} || {{apitype|number}} || 
|-
| {{apiname|marginRight}} || {{apitype|number}} || 
|-
| {{apiname|marginBottom}} || {{apitype|number}} || 
|-
| {{apiname|sliceMode}} || {{apitype|Enum.UITextureSliceMode}} || 
|}

{{:Enum.UITextureSliceMode}}

==Patch changes==
* {{Patch 8.1.0|note=Changed to <code>C_Texture.GetAtlasInfo()</code> and returns structured data.<sup>[https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#260]</sup>}}
* {{Patch 6.0.2|note=Added as <code>GetAtlasInfo()</code>.}}

==See also==
* [[API Texture GetAtlas|Texture:GetAtlas]]()
* [[API Texture SetAtlas|Texture:SetAtlas]]()
* UI [https://www.townlong-yak.com/framexml/go/CreateAtlasMarkup CreateAtlasMarkup] - Returns an inline [[UI_escape_sequences#Textures|fontstring texture]] from an atlas
* [https://www.townlong-yak.com/framexml/live/Helix/AtlasInfo.lua Helix/AtlasInfo.lua] - Lua table containing atlas info
* {{dbc|uitextureatlasmember|UiTextureAtlasMember.db2}} - DBC for atlases
* [https://www.curseforge.com/wow/addons/textureatlasviewer Texture Atlas Viewer] - Addon for browsing atlases in-game
```