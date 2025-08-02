# API C VignetteInfo.GetVignettePosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_VignetteInfo|system=Vignette}}
Needs summary.
 vignettePosition, vignetteFacing = C_VignetteInfo.GetVignettePosition(vignetteGUID, uiMapID)

==Arguments==
:;vignetteGUID:{{apitype|WOWGUID}}
:;uiMapID:{{apitype|number}}

==Returns==
:;vignettePosition:{{apitype|vector2}}
:;vignetteFacing:{{apitype|number?}}

==Patch changes==
* {{Patch 10.1.0|note=Added <code>vignetteFacing</code> return.}}
* {{Patch 8.0.1|note=Added.}}
```