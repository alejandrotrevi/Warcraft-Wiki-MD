# API UnitEffectiveLevel

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the unit's effective (scaled) level.
 level = UnitEffectiveLevel(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;level:{{apitype|number}}

==Details==
* When [[Drunk#Gameplay_effects|inebriated]], the apparent level of hostile units is lowered by up to 5.

==See also==
* {{api|UnitLevel}}
```