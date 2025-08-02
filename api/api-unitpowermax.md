# API UnitPowerMax

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the maximum power resource of the unit.
 maxPower = UnitPowerMax(unitToken [, powerType [, unmodified]])

==Arguments==
:;unitToken:{{apitype|string}} : [[UnitId]]
:;powerType:{{apitype|Enum.PowerType?}} - Type of resource (mana/rage/energy/etc) to query
:;unmodified:{{apitype|boolean?}} - Return the higher precision internal value (for graphical use only)

==Returns==
:;maxPower:{{apitype|number}} - The unit's maximum amount of the queried resource.

==Details==
* If no type is specified, UnitPowerMax returns the current primary type, e.g., energy for a druid in cat form.
* You can determine the current primary power type via {{api|UnitPowerType}}()

==Example==
Prints the maximum amount of mana for the player.
 /dump UnitPowerMax("player", Enum.PowerType.Mana)

==Patch changes==
* {{Patch 3.0.2|note=Added, replaces {{api|UnitManaMax}}()}}
```