# API GetComboPoints

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the amount of current combo points.
 comboPoints = GetComboPoints(unit, target)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - Normally "player" or "vehicle".
:;target:{{apitype|string}} : [[UnitId]] - Normally "target".

==Returns==
:;comboPoints:{{apitype|number}} - Number of combo points unit has on target; between 0 and 5 inclusive.

==Details==
* {{api|t=e|UNIT_COMBO_POINTS}} fires when combo points are updated. It fires every 10 second outside of combat if the rogue have shared combo points, it contiuse to fire every 10 second until combo point pool is empty.
* {{Patch 6.0|note=Combo Points for rogues are now shared across all targets and they are no longer lost when switching targets.|comment=GetComboPoints will return 0 if target is friendly or not found. Use '''[[API_UnitPower|UnitPower]]([[unitId]], 4)''' to get combo points without an enemy targeted.}}

==See also==
* [[API_UnitPower|UnitPower]]
```