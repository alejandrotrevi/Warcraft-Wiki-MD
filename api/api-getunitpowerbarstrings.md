# API GetUnitPowerBarStrings

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Needs summary.
 name, tooltip, cost = GetUnitPowerBarStrings(unitToken)
                     = GetUnitPowerBarStringsByID(barID)

==Arguments==
===<font color="#4ec9b0">GetUnitPowerBarStrings</font>===
:;unitToken:{{apitype|string}} : [[UnitId]]

===<font color="#4ec9b0">GetUnitPowerBarStringsByID</font>===
:;barID:{{apitype|number}} - from {{api|UnitPowerBarID}}()

==Returns==
:;name:{{apitype|string?}}
:;tooltip:{{apitype|string?}}
:;cost:{{apitype|string?}}

==Patch changes==
* {{Patch 8.3.0|note=Added. Replaces <code>GetAlternatePowerInfoByID()</code> which is deprecated. [https://www.townlong-yak.com/framexml/8.3.0/Blizzard_Deprecated/Deprecated_8_3_0.lua#27]}}
```