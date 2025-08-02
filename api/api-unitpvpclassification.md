# API UnitPvpClassification

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns whether the unit is a flag/orb carrier or cart runner.
 classification = UnitPvpClassification(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;classification:{{apitype|Enum.PvPUnitClassification?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| align="center" | 0 || FlagCarrierHorde || 
|-
| align="center" | 1 || FlagCarrierAlliance || 
|-
| align="center" | 2 || FlagCarrierNeutral || 
|-
| align="center" | 3 || CartRunnerHorde || 
|-
| align="center" | 4 || CartRunnerAlliance || 
|-
| align="center" | 5 || AssassinHorde || 
|-
| align="center" | 6 || AssassinAlliance || 
|-
| align="center" | 7 || OrbCarrierBlue || 
|-
| align="center" | 8 || OrbCarrierGreen || 
|-
| align="center" | 9 || OrbCarrierOrange || 
|-
| align="center" | 10 || OrbCarrierPurple || 
|}

==Patch changes==
* {{Patch 8.1.5|note=Added.}}
```