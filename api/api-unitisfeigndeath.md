# API UnitIsFeignDeath

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns true if the unit (must be a group member) is feigning death.
 isFeign = UnitIsFeignDeath(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;isFeign:{{apitype|boolean}} - Returns true if the checked unit is feigning death, false otherwise.

==Details==
* Only provides valid data for friendly units.
* Does not work for the player character. Use {{api|UnitAura}} instead:
 isFeign = UnitAura("player", "Feign Death") ~= nil

==Patch changes==
* {{Patch 2.1.0|note=Replaced <code>IsFeignDeath</code>.}}
```