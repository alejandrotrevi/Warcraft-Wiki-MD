# API C LegendaryCrafting.GetRuneforgePowersByClassSpecAndCovenant

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LegendaryCrafting|system=LegendaryCrafting}}
Needs summary.
 runeforgePowerIDs = C_LegendaryCrafting.GetRuneforgePowersByClassSpecAndCovenant([classID [, specID [, covenantID [, filter]]]])

==Arguments==
:;classID:{{apitype|number?}} : [[ClassId]]
:;specID:{{apitype|number?}} : [[SpecializationID]]
:;covenantID:{{apitype|number?}}
:;filter:{{apitype|Enum.RuneforgePowerFilter?}}
{{:Enum.RuneforgePowerFilter|nocaption=1}}

==Returns==
:;runeforgePowerIDs:{{apitype|number[]}}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```