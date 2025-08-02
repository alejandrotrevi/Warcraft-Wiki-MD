# API IsFalling

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns true if the specified unit is currently falling.
 falling = IsFalling([unit])

==Arguments==
:;unit:{{apitype|UnitToken?}} - A unitID to query. Defaults to player if omitted.

==Returns==
:;falling:{{apitype|boolean}} - true if the unit is currently falling, false otherwise.
```