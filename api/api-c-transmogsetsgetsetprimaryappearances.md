# API C TransmogSets.GetSetPrimaryAppearances

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TransmogSets|system=TransmogrifySets}}
Needs summary.
 apppearances = C_TransmogSets.GetSetPrimaryAppearances(transmogSetID)

==Arguments==
:;transmogSetID:{{apitype|number}} : [[TransmogSetID]]

==Returns==
:;apppearances:{{apitype|TransmogSetPrimaryAppearanceInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| appearanceID || {{apitype|number}} || 
|-
| collected || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Added. Replaces {{api|C_TransmogSets.GetSetSources}}()}}
```