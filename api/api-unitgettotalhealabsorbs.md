# API UnitGetTotalHealAbsorbs

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the total amount of healing the unit can absorb without gaining health.
 totalHealAbsorbs = UnitGetTotalHealAbsorbs(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;totalHealAbsorbs:{{apitype|number}} - amount of healing the unit can absorb without gaining health.

==Details==
* Abilities like [[Necrotic Strike]] cause affected units to absorb healing without gaining health.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}

==See also==
* {{api|t=e|UNIT_HEAL_ABSORB_AMOUNT_CHANGED}}
```