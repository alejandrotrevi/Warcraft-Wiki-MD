# API GetUnitPowerBarTextureInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Needs summary.
 texture, colorR, colorG, colorB, colorA = GetUnitPowerBarTextureInfo(unitToken, textureIndex [, timerIndex])
                                         = GetUnitPowerBarTextureInfoByID(barID, textureIndex)

==Arguments==
===<font color="#4ec9b0">GetUnitPowerBarTextureInfo</font>===
:;unitToken:{{apitype|string}} : [[UnitId]]
:;textureIndex:{{apitype|number}}
:;timerIndex:{{apitype|number?}}

===<font color="#4ec9b0">GetUnitPowerBarTextureInfoByID</font>===
:;barID:{{apitype|number}}
:;textureIndex:{{apitype|number}}

==Returns==
:;texture:{{apitype|number}}
:;colorR:{{apitype|number}}
:;colorG:{{apitype|number}}
:;colorB:{{apitype|number}}
:;colorA:{{apitype|number}}

==Patch changes==
* {{Patch 8.3.0|note=Added. Replaces <code>UnitAlternatePowerTextureInfo()</code> [https://www.townlong-yak.com/framexml/8.3.0/Blizzard_Deprecated/Deprecated_8_3_0.lua#36]}}
```