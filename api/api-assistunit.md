# API AssistUnit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=TargetScript}} {{restrictedapi|protected|note=Use the "assist" action type of [[SecureActionButtonTemplate]], or the [[MACRO assist|/assist]] slash command.}}
Assists the unit by targeting the same target.
 AssistUnit(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Details==
* If the players target was changed by a [[World of Warcraft API#Targetting Functions|Targetting Function]] it is possible to restore the original target by assisting the player.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
```