# API UpdateWorldMapArrow

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Rotates a texture based on the direction the player is currently {{api|GetPlayerFacing|facing}}.
 UpdateWorldMapArrow(arrowFrame)

==Arguments==
:;arrowFrame:Widget - any Texture widget, although <code>Interface\Minimap\MinimapArrow</code> is the intended texture.

==Details==
* This function applies a {{api|Texture:SetTexCoord|t=w}} transformation rotating the texture.
* The transformation ensures that the visible portion of the original texture remains of a consistent size. This size is slightly smaller than the original (unrotated) texture.

==Patch changes==
* {{Patch 5.2.0|note=Added.}}
```