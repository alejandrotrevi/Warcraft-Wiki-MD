# API C PvP.GetGlobalPvpScalingInfoForSpecID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 pvpScalingData = C_PvP.GetGlobalPvpScalingInfoForSpecID(specializationID)

==Arguments==
:;[[SpecializationID|specializationID]]:{{apitype|number}}

==Returns==
:;pvpScalingData:structure - PvpScalingData[]
{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| scalingDataID || {{apitype|number}} || 
|-
| specializationID || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| value || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 7.2.0|note=Added.}}
```