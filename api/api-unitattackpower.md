# API UnitAttackPower

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the unit's melee attack power and modifiers.
 base, posBuff, negBuff = UnitAttackPower(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit to get information from. (Does not work for <code>"target"</code> - Possibly only <code>"player"</code> and <code>"pet"</code>)

==Returns==
:;base:{{apitype|number}} - The unit's base attack power
:;posBuff:{{apitype|number}} - The total effect of positive buffs to attack power.
:;negBuff:{{apitype|number}} - The total effect of negative buffs to the attack power (a negative number)

==Example==
Displays the player's current attack power in the default chat window.
<syntaxhighlight lang="lua">
local base, posBuff, negBuff = UnitAttackPower("player")
local effective = base + posBuff + negBuff
print("Your current attack power: "..effective)
</syntaxhighlight>
```