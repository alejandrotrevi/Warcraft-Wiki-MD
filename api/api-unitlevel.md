# API UnitLevel

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the level of the unit.
 level = UnitLevel(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - For example <code>"player"</code> or <code>"target"</code>

==Returns==
:;level:{{apitype|number}} - The unit level. Returns <code>-1</code> for boss units or hostile units 10 levels above the player (Level ??).

==Details==
* When calling <code>UnitLevel("player")</code> on {{api|t=e|PLAYER_LEVEL_UP}} it might be incorrect, check the payload instead to be sure.
* When [[Drunk#Gameplay_effects|inebriated]], the apparent level of hostile units is lowered by up to 5.
{| {{apitable}}
{{apirow | Related API | {{api|UnitEffectiveLevel}} }}
{{apirow | Related Events | {{api|t=e|PLAYER_LEVEL_UP}}<br>{{api|t=e|PLAYER_LEVEL_CHANGED}} }}
|}
```