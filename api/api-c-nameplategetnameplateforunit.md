# API C NamePlate.GetNamePlateForUnit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the nameplate for a unit.
 nameplate = C_NamePlate.GetNamePlateForUnit(unit [, isSecure])

==Arguments==
:;unit:{{apitype|UnitToken}}
:;isSecure:{{apitype|boolean?}} - If protected nameplates for friendly units while in instanced areas should be returned.

==Returns==
:;nameplate:{{apitype|Nameplate?}} : {{api|t=o|Frame}}|[https://github.com/Gethe/wow-ui-source/blob/10.2.0/Interface/AddOns/Blizzard_NamePlates/Blizzard_NamePlates.lua#L540 NamePlateBaseMixin]
<onlyinclude>{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| UnitFrame || {{apitype|Button}} || 
|-
| driverFrame || {{apitype|NamePlateDriverFrame}} || points to [https://github.com/Gethe/wow-ui-source/blob/10.2.0/Interface/AddOns/Blizzard_NamePlates/Blizzard_NamePlates.xml#L5 NamePlateDriverFrame] ({{Framexml link|AddOns/Blizzard_NamePlates/Blizzard_NamePlates.lua|name=NamePlateDriverMixin}}) 
|-
| namePlateUnitToken || {{apitype|string}} || e.g. <code>"nameplate1"</code>
|-
| template || {{apitype|string}} || e.g. <code>"NamePlateUnitFrameTemplate"</code>
|-
! colspan="3" | NamePlateBaseMixin
|-
| [https://www.townlong-yak.com/framexml/go/NamePlateBaseMixin:OnAdded OnAdded] || {{apitype|function}} || 
|-
| [https://www.townlong-yak.com/framexml/go/NamePlateBaseMixin:OnRemoved OnRemoved] || {{apitype|function}} || 
|-
| [https://www.townlong-yak.com/framexml/go/NamePlateBaseMixin:OnOptionsUpdated OnOptionsUpdated] || {{apitype|function}} || 
|-
| [https://www.townlong-yak.com/framexml/go/NamePlateBaseMixin:ApplyOffsets ApplyOffsets] || {{apitype|function}} || 
|-
| [https://www.townlong-yak.com/framexml/go/NamePlateBaseMixin:GetAdditionalInsetPadding GetAdditionalInsetPadding] || {{apitype|function}} || 
|-
| [https://www.townlong-yak.com/framexml/go/NamePlateBaseMixin:GetPreferredInsets GetPreferredInsets] || {{apitype|function}} || 
|-
| [https://www.townlong-yak.com/framexml/go/NamePlateBaseMixin:OnSizeChanged OnSizeChanged] || {{apitype|function}} || 
|}</onlyinclude>
```