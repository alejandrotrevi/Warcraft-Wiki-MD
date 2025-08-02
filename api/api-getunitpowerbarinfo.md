# API GetUnitPowerBarInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Needs summary.
 info = GetUnitPowerBarInfo(unitToken)
      = GetUnitPowerBarInfoByID(barID)

==Arguments==
===<font color="#4ec9b0">GetUnitPowerBarInfo</font>===
:;unitToken:{{apitype|string}} : [[UnitId]]

===<font color="#4ec9b0">GetUnitPowerBarInfoByID</font>===
:;barID:{{apitype|number}} - from {{api|UnitPowerBarID}}()

==Returns==
:;info:{{apitype|UnitPowerBarInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| ID || {{apitype|number}} || 
|-
| barType || {{apitype|number}} || 
|-
| minPower || {{apitype|number}} || 
|-
| startInset || {{apitype|number}} || 
|-
| endInset || {{apitype|number}} || 
|-
| smooth || {{apitype|boolean}} || 
|-
| hideFromOthers || {{apitype|boolean}} || 
|-
| showOnRaid || {{apitype|boolean}} || 
|-
| opaqueSpark || {{apitype|boolean}} || 
|-
| opaqueFlash || {{apitype|boolean}} || 
|-
| anchorTop || {{apitype|boolean}} || 
|-
| forcePercentage || {{apitype|boolean}} || 
|-
| sparkUnderFrame || {{apitype|boolean}} || 
|-
| flashAtMinPower || {{apitype|boolean}} || 
|-
| fractionalCounter || {{apitype|boolean}} || 
|-
| animateNumbers || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 8.3.0|note=Added. Replaces <code>UnitAlternatePowerInfo()</code> and <code>UnitAlternatePowerCounterInfo()</code> which are deprecated. [https://www.townlong-yak.com/framexml/8.3.0/Blizzard_Deprecated/Deprecated_8_3_0.lua#27]}}
```