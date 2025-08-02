# API C Transmog.CanTransmogItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Transmog|system=Transmogrify}}
Needs summary.
 canBeTransmogged, selfFailureReason, canTransmogOthers, othersFailureReason = C_Transmog.CanTransmogItem(itemInfo)

==Arguments==
:;itemInfo:{{apitype|number,string}} : {{:ItemInfo}}

==Returns==
:;canBeTransmogged:{{apitype|boolean}}
:;selfFailureReason:{{apitype|string?}}
:;canTransmogOthers:{{apitype|boolean}}
:;othersFailureReason:{{apitype|string?}}

==Patch changes==
* {{Patch 9.1.0|note=Added. Replaces {{api|C_Transmog.GetItemInfo}}()}}

==See also==
* {{api|C_Transmog.CanTransmogItemWithItem}}()
```