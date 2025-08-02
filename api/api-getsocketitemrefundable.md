# API GetSocketItemRefundable

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the item currently being socketed is refundable.
 isRefundable = GetSocketItemRefundable()

==Returns==
:;isRefundable:{{apitype|boolean}} - 1 if the item selected for socketing can be returned to a merchant for a refund.

==Details==
* Items purchased with non-gold currencies can sometimes be sold back to a merchant for a full refund within a limited time frame.
* The item remains refundable if you socket gems into it; however, any socketed gems will not be refunded upon selling the item back to a vendor.

==See also==
* {{api|GetSocketItemBoundTradeable}}
```