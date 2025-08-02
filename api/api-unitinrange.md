# API UnitInRange

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}} {{restrictedapi|grouponly}}
Returns true if the unit is within 40 yards range (25 yards for Evokers).
 inRange, checkedRange = UnitInRange(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;inRange:{{apitype|boolean}} - true if the unit is within 40 (25 for Evokers) yards of the player
:;checkedRange:{{apitype|boolean}} - true if a range check was actually performed; false if the information about distance to the queried unit is unavailable.

Note: UnitInRange("player") will return false, false outside of a group.

==Patch changes==
* {{Patch 5.0.4|note=Added <code>checkedRange</code> return value.}}
```