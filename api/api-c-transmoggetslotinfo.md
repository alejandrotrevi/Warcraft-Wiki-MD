# API C Transmog.GetSlotInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Transmog|system=Transmogrify}}
Returns info for a transmog slot.
 isTransmogrified, hasPending, isPendingCollected, canTransmogrify, cannotTransmogrifyReason, hasUndo, isHideVisual, texture = C_Transmog.GetSlotInfo(transmogLocation)

==Arguments==
:;transmogLocation:{{apitype|TransmogLocationMixin}}

==Returns==
:;isTransmogrified:{{apitype|boolean}}
:;hasPending:{{apitype|boolean}} - If the item is pending transmogrification
:;isPendingCollected:{{apitype|boolean}}
:;canTransmogrify:{{apitype|boolean}}
:;cannotTransmogrifyReason:{{apitype|number}} - The error reason index if <code>canTransmogrify</code> is false. See [https://www.townlong-yak.com/framexml/8.1.5/Constants.lua#889 TRANSMOG_INVALID_CODES] and [https://www.townlong-yak.com/framexml/8.1.5/GlobalStrings.lua#14590 TRANSMOGRIFY_INVALID]
:;hasUndo:{{apitype|boolean}} - If the item is pending detransmogrification
:;isHideVisual:{{apitype|boolean}} - If the appearance hides the gear, e.g. [[Hidden Helm]]
:;texture:{{apitype|number?}} : [[FileID]]

==Patch changes==
* {{Patch 9.0.1|note=Added TransmogLocationMixin argument.}}
* {{Patch 7.0.3|note=Moved to <code>C_Transmog.GetSlotInfo()</code>}}
* {{Patch 4.3.0|note=Added as <code>GetTransmogrifySlotInfo()</code>}}
```