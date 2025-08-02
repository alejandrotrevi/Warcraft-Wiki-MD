# API UnitGetTotalAbsorbs

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the total amount of damage the unit can absorb before losing health.
 totalAbsorbs = UnitGetTotalAbsorbs(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit to query absorption shields of.

==Returns==
:;totalAbsorbs:{{apitype|number}} - total amount of damage the unit can take without losing health.

==Patch changes==
* {{Patch 5.2.0|note=Added.}}

==See also==
* {{api|t=e|UNIT_ABSORB_AMOUNT_CHANGED}}
```