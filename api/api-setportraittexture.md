# API SetPortraitTexture

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Sets a texture to a unit's 2D portrait.
 SetPortraitTexture(textureObject, unitToken [, disableMasking])

==Arguments==
:;textureObject:{{apitype|SimpleTexture}}
:;unitToken:{{apitype|UnitToken}}
:;disableMasking:{{apitype|boolean?|default=false}}

==Example==
<syntaxhighlight lang="lua">
local f = CreateFrame("Frame")
f:SetPoint("CENTER")
f:SetSize(64, 64)

f.tex = f:CreateTexture()
f.tex:SetAllPoints(f)
SetPortraitTexture(f.tex, "player")
</syntaxhighlight>
[[File:API SetPortraitTexture.png]]

==Patch changes==
* {{Patch 10.0.0|note=Added <code>disableMasking</code> argument.}}
```