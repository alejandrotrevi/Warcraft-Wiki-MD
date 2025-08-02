# API CombatTextSetActiveUnit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Changes the entity for which {{api|t=e|COMBAT_TEXT_UPDATE}} events fire.
 CombatTextSetActiveUnit(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The the entity you want to receive notifications for.

==Details==
* The event is tied to the entity rather than the unit -- thus, if you call CombatTextSetActiveUnit("target") and then target something else, you'll get notifications for the unit you were targeting when calling the function, rather than your new target.
* Only one unit can be "active" at a time.
* The {{api|COMBAT_TEXT_UPDATE|t=e}} event is used in to provide part of Blizzard's Floating Combat Text functionality; it fires to notify of aura gains/losses and incoming damage and heals.

==See Also==
* {{api|COMBAT_TEXT_UPDATE|t=e}}
```