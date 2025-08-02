# API C Transmog.ClearPending

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Transmog|system=Transmogrify}}
Clears an equipment slot of pending transmogs.
 C_Transmog.ClearPending(transmogLocation)

==Arguments==
:;transmogLocation:{{apitype|TransmogLocationMixin}}

==Details==
* Triggers {{api|t=e|TRANSMOGRIFY_UPDATE}}

==Patch changes==
* {{Patch 9.0.1|note=Takes a TransmogLocationMixin.}}
* {{Patch 7.0.3|note=Moved from {{api|ClearTransmogrifySlot}}() to {{api|C_Transmog.ClearPending}}())}}
```