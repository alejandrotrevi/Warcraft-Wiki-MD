# API IsSwimming

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns true if the specified unit is currently swimming.
 isSwimming = IsSwimming(unit)

==Arguments==
:;unit:{{apitype|UnitToken?}} - A unitID to query. Defaults to player if omitted.

==Returns==
:;isSwimming:{{apitype|boolean}} - True if the unit is swimming, false otherwise.

==Details==
* A swimming character's movement speed is based on their swim speed (per {{api|GetUnitSpeed}}).
* In some locations and when affected by certain effects, player characters can ''run'' at the bottom of the ocean/lake/etc. In those cases, the player is not considered swimming (but is still submerged per {{api|IsSubmerged}}).
* This function is available within the [[RestrictedEnvironment]]

==See also==
* {{api|IsSubmerged}}
* {{api|IsFlying}}
```