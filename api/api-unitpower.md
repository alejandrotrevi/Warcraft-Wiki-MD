# API UnitPower

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the current power resource of the unit.
 power = UnitPower(unitToken [, powerType [, unmodified]])

==Arguments==
:;unitToken:{{apitype|string}} : [[UnitId]]
:;powerType:{{apitype|Enum.PowerType?|link=1}} - Type of resource (mana/rage/energy/etc) to query
:;unmodified:{{apitype|boolean?}} - Return the higher precision internal value (for graphical use only)

==Returns==
:;power:{{apitype|number}} - the unit's current power level

==Details==
* If no type is specified, UnitPower returns the current primary type, e.g., energy for a druid in cat form.
* You can determine the current primary power type via {{api|UnitPowerType}}()
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|UNIT_POWER_UPDATE}}<br>{{api|t=e|UNIT_POWER_FREQUENT}} }}
{{apirow | Related API | {{api|UnitPowerType}}, {{api|UnitPowerMax}} }}
|}

==Example==
Prints the current amount of mana for the player.
 /dump UnitPower("player", Enum.PowerType.Mana)

==Patch changes==
* {{Patch 3.0.2|note=Added, replaces {{api|UnitMana}}()}}
```