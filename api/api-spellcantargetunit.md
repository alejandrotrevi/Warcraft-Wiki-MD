# API SpellCanTargetUnit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the spell awaiting target selection can be cast on the unit.
 canTarget = SpellCanTargetUnit(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit to check.

==Returns==
:;canTarget:{{apitype|boolean}} - Whether the spell can target the given unit.

==Details==
: This will check for range, but not for LOS.
```