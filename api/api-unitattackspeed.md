# API UnitAttackSpeed

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the unit's melee attack speed for each hand.
 mainSpeed, offSpeed = UnitAttackSpeed(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit to get information from. (Verified for <code>"player"</code> and <code>"target"</code>)

==Returns==
:;mainSpeed:{{apitype|number}} - The unit's base main hand attack speed (seconds)
:;offSpeed:{{apitype|number}} - The unit's offhand attack speed (seconds) - <code>nil</code> if the unit has no offhand weapon.
```