# API SetPortraitToTexture

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Applies a circular mask to a texture, making it resemble a portrait.
 SetPortraitToTexture(texture, path)

==Arguments==
:;texture:{{apitype|Texture}}
:;path:{{apitype|TextureAssetDisk}}

==Details==
* This function only accepts texture assets that have dimensions of 64x64 or smaller. Larger textures will raise an "Texture is not 64x64 pixels" error.
** For larger textures, consider instead using [[UIOBJECT MaskTexture|MaskTexture]] objects which do not suffer from this same limitation.

==Example==
<syntaxhighlight lang="lua">
local tex = UIParent:CreateTexture()
tex:SetPoint("CENTER")
tex:SetSize(64, 64)
SetPortraitToTexture(tex, "interface/icons/inv_mushroom_11")
</syntaxhighlight>
[[File:API SetPortraitToTexture.png]]

==Patch changes==
* {{Patch 10.2.0|note=The <code>texture</code> parameter must now be a texture object. Previously, it could be a string that named a global texture object.}}

==See also==
* {{api|t=o|MaskTexture}}
```