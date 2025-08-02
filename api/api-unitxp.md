# API UnitXP

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the current XP of the unit; only works on the player.
 xp = UnitXP(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;xp:{{apitype|number}} - Returns the current XP points of the unit.

==Details==
* This does '''not''' work for hunter pets, use {{api|GetPetExperience}}() for that.
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|PLAYER_XP_UPDATE}} }}
{{apirow | Related API | {{api|UnitXPMax}} }}
|}

==Example==
<onlyinclude><syntaxhighlight lang="lua">
local xp = UnitXP("player")
local nextXP = UnitXPMax("player")
print(string.format("Your XP is currently at %.1f%%", xp / nextXP * 100))
</syntaxhighlight></onlyinclude>
```