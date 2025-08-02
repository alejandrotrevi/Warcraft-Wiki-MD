# API GetObjectIconTextureCoords

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns texture coordinates of an object icon.
 left, right, top, bottom = GetObjectIconTextureCoords(objectIcon)

==Arguments==
:;objectIcon:{{apitype|number}} - index of the object icon to retrieve texture coordinates for, ascending from -2.

==Returns==
:;left:{{apitype|number}} - left edge of the specified icon, 0 for the texture's left edge and 1 for the texture's right edge.
:;right:{{apitype|number}} - right edge of the specified icon, 0 for the texture's left edge and 1 for the texture's right edge.
:;top:{{apitype|number}} - top edge of the specified icon, 0 for the texture's top edge and 1 for the texture's bottom edge.
:;bottom:{{apitype|number}} - bottom edge of the specified icon, 0 for the texture's top edge and 1 for the texture's bottom edge.

==Details==
[[File:OBJECTICONS.png|thumb|OBJECTICONS.blp]]
* Returns texture coordinates into Interface\MINIMAP\OBJECTICONS.blp, the {{api|t=w|Minimap:SetBlipTexture|minimap blip texture}}.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}
```