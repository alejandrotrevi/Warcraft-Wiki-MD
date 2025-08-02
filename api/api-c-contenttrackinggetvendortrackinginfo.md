# API C ContentTracking.GetVendorTrackingInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ContentTracking|system=ContentTracking}}
Needs summary.
 vendorTrackingInfo = C_ContentTracking.GetVendorTrackingInfo(collectableEntryID)

==Arguments==
:;collectableEntryID:{{apitype|number}}

==Returns==
:;vendorTrackingInfo:{{apitype|VendorTrackingInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| creatureName || {{apitype|string}} || 
|-
| zoneName || {{apitype|string?}} || 
|-
| currencyType || {{apitype|number?}} || 
|-
| cost || {{apitype|BigUInteger?}} || 
|}
```