# API UnitRangedAttack

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the unit's ranged attack and modifier.
 base, modifier = UnitRangedAttack(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - Likely only works for <code>"player"</code> and <code>"pet"</code>

==Returns==
:;base:{{apitype|number}} - The unit's base ranged attack number (0 if no ranged weapon is equipped)
:;modifier:{{apitype|number}} - The total effect of all modifiers (positive and negative) to ranged attack.

==Example==
 local base, modifier = UnitRangedAttack("player");
 local effective = base + modifier;
 message(effective);
===Result===
Displays a message containing your effective ranged attack skill([[Weapon Skill]]).
```