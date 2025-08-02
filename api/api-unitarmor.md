# API UnitArmor

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the armor stats for the unit.
<syntaxhighlight lang="lua">
base, effectiveArmor, armor, bonusArmor       = UnitArmor(unit) -- retail
base, effectiveArmor, armor, posBuff, negBuff = UnitArmor(unit) -- classic
</syntaxhighlight>

==Arguments==
:;unit:{{apitype|UnitToken}} - Only works for <code>"player"</code> and <code>"pet"</code>. Works for <code>"target"</code> with Hunter's Beast Lore.

==Returns==
:;base:{{apitype|number}} - The unit's base armor.
:;effectiveArmor:{{apitype|number}} - The unit's effective armor.
:;armor:{{apitype|number}}
====<font color="#4ec9b0">Retail</font>====
:;bonusArmor:{{apitype|number}}
====<font color="#4ec9b0">Classic</font>====
:;posBuff:{{apitype|number}} - Amount of armor increase due to positive buffs
:;negBuff:{{apitype|number}} - Amount of armor reduction due to negative buffs (a negative number)

==Example==
<syntaxhighlight lang="lua">
local base, effectiveArmor = UnitArmor("player")
print(format("Your current armor is %d (%d base)", effectiveArmor, base))
</syntaxhighlight>
```