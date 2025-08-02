# API C TooltipInfo.GetHyperlink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TooltipInfo|system=TooltipInfo}} {{api dftooltip}}
Returns tooltip data for a given hyperlink.
 data = C_TooltipInfo.GetHyperlink(hyperlink [, optionalArg1 [, optionalArg2 [, hideVendorPrice]]])

 GameTooltip:[[API_GameTooltip_SetHyperlink|SetHyperlink]](...)

==Arguments==
:;hyperlink:{{apitype|string}} - [[Hyperlink]] : The hyperlink to query.
:;optionalArg1:{{apitype|number?}} - First optional argument for the given link. Refer to the Optional Arguments table below for details.
:;optionalArg2:{{apitype|number?}} - Second optional argument for the given link. Refer to the Optional Arguments table below for details.
:;hideVendorPrice:{{apitype|boolean?}} - If true, omits vendor price information from the line text data.

{| class="darktable zebra" style="margin-left: 3.9em"
|+ Optional Arguments
|-
! Link Type !! optionalArg1 !! optionalArg2 !! Details
|-
| [[itemLink|item]] || [[ClassId|classID]] || [[SpecializationID|specID]] ||
|-
| [[spellLink|spell]] || [[DifficultyID|difficultyID]] || [[ContentTuningID|contentTuningID]] ||
|}

==Returns==
:;data:{{apitype|TooltipData}}
{{:Struct TooltipData|nocaption=1}}

==Patch changes==
* {{Patch 10.0.2|note=Added.}}
```