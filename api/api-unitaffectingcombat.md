# API UnitAffectingCombat

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns true if the unit is in combat.
 affectingCombat = UnitAffectingCombat(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit to check.

==Returns==
:;affectingCombat:{{apitype|boolean}} - Returns true if the unit is in combat or has aggro, false otherwise.

==Details==
Note: some of the information below seems incorrect or outdated. You may wish to test various situations yourself, if they are relevant for your usecase.
* The unit need not be in combat with you as the player specifically.
* Returns true when initiating combat.
* Returns true if aggroed, even if enemy doesn't land a blow.
* For hunters, it returns true shortly after pet enters combat.
* If using timed spell such as aimed shot, returns true when spell fires (not during charge up).
* Returns to false on death.
* Returns false if the unit being checked for aggro is out of range, or in another zone.
* Returns false if a unit is proximity-aggroed. It won’t return true until it either attacks or is attacked.
```