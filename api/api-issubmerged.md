# API IsSubmerged

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns whether the player character is submerged in water.
 isSubmerged = IsSubmerged([unit])

==Arguments==
:;unit:{{apitype|UnitToken?}}

==Returns==
:;isSubmerged:{{apitype|boolean}} - True if the unit is submerged.

==Details==
* This function is similar to {{api|IsSwimming}}, but also returns 1 when running at the bottom of a surface of water.
* This function is available within the [[RestrictedEnvironment]]

==See also==
* {{api|IsSwimming}}
* {{api|IsFlying}}
```