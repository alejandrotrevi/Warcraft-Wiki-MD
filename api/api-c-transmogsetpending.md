# API C Transmog.SetPending

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Transmog|system=Transmogrify}}
Applies a pending transmog choice to the given TransmogLocation slot.
 C_Transmog.SetPending(transmogLocation, pendingInfo)

==Arguments==
:;transmogLocation:{{apitype|TransmogLocationMixin}}
:;pendingInfo:{{apitype|TransmogPendingInfoMixin}}

==Patch changes==
* {{Patch 9.1.0|note=Replaced <code>transmogID, categoryID</code> arguments with <code>pendingInfo</code>}}
* {{Patch 9.0.1|note=Replaced <code>slotID, transmogType</code> arguments with <code>transmogLocation</code>}}
* {{Patch 7.0.3|note=Added.}}
```