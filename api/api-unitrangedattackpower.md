# API UnitRangedAttackPower

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the ranged attack power of the unit.
 attackPower, posBuff, negBuff = UnitRangedAttackPower(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - Likely only works for <code>"player"</code> and <code>"pet"</code>

==Returns==
:;attackPower:{{apitype|number}} - The unit's base ranged attack power (seems to give a positive number even if no ranged weapon equipped)
:;posBuff:{{apitype|number}} - The total effect of positive buffs to ranged attack power.
:;negBuff:{{apitype|number}} - The total effect of negative buffs to the ranged attack power (a negative number)

==Example==
Shows your current ranged attack power.
 local base, posBuff, negBuff = UnitRangedAttackPower("player");
 local effective = base + posBuff + negBuff;
 print("Your current ranged attack power: " .. effective);
```