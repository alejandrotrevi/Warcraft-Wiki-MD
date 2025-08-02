# API GetTrackingTexture

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the texture of the active tracking buff.
 icon = GetTrackingTexture()

==Returns==
:;icon:{{apitype|number}} : [[FileID]] - The texture of the active tracking buff, or <code>nil</code> if noone.

==Patch changes==
* {{Patch 4.0.1|note=Removed. {{api|GetTrackingInfo}}() can be used to find icons for specific tracking types; multiple tracking types can be enabled at the same time.}}
```