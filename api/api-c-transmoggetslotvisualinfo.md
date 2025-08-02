# API C Transmog.GetSlotVisualInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Transmog|system=Transmogrify}}
Needs summary.
 baseSourceID, baseVisualID, appliedSourceID, appliedVisualID, pendingSourceID, pendingVisualID, hasUndo, isHideVisual, itemSubclass = C_Transmog.GetSlotVisualInfo(transmogLocation)

==Arguments==
:;transmogLocation:{{apitype|TransmogLocationMixin}}

==Returns==
:;baseSourceID:{{apitype|number}}
:;baseVisualID:{{apitype|number}}
:;appliedSourceID:{{apitype|number}}
:;appliedVisualID:{{apitype|number}}
:;pendingSourceID:{{apitype|number}}
:;pendingVisualID:{{apitype|number}}
:;hasUndo:{{apitype|boolean}}
:;isHideVisual:{{apitype|boolean}}
:;itemSubclass:{{apitype|number}}

==Patch changes==
* {{Patch 9.1.0|note=Removed <code>pendingCategoryID, appliedCategoryID</code> returns.}}
* {{Patch 9.0.1|note=Added.}}
```