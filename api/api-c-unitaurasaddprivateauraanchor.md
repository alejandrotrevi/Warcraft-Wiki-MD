# API C UnitAuras.AddPrivateAuraAnchor

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UnitAuras|system=UnitAuras}}
Needs summary.
 anchorID = C_UnitAuras.AddPrivateAuraAnchor(args)

==Arguments==
:;args:{{apitype|AddPrivateAuraAnchorArgs}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| unitToken || {{apitype|string}} || 
|-
| auraIndex || {{apitype|number}} || 
|-
| parent || {{apitype|Frame}} || 
|-
| showCountdownFrame || {{apitype|boolean}} || 
|-
| showCountdownNumbers || {{apitype|boolean}} || 
|-
| iconInfo || {{apitype|PrivateAuraIconInfo?}} || 
|-
| durationAnchor || {{apitype|AnchorBinding?}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ PrivateAuraIconInfo
! Field !! Type !! Description
|-
| iconAnchor || {{apitype|AnchorBinding}} || 
|-
| iconWidth || {{apitype|uiUnit}} || 
|-
| iconHeight || {{apitype|uiUnit}} || 
|}

{{:Struct AnchorBinding}}

==Returns==
:;anchorID:{{apitype|number?}}
```