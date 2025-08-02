# API AttackTarget

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=TargetScript}} {{restrictedapi|protected|note=Use the [[startattack|/startattack]] slash command.}}
Toggles auto-attacking of the current target.
 AttackTarget()

==Details==
* This is actually a toggle.  If not currently attacking, it will initiate attack.  If currently attacking, it will stop attacking.
* You can test your current attack "Action slot" using [[API_IsCurrentAction|IsCurrentAction(actionSlot)]] for status (you'll have to find the auto-attack slot, though).
* If you need a way to always engage auto-attack, rather than toggle it on or off, one workaround is [[API_AssistUnit|AssistUnit("player")]] this will always attack if you have "Attack on assist" checked in the Advanced tab of the Interface Options panel. Note that you cannot combine this with [[API_TargetNearestEnemy|TargetNearestEnemy()]] in the same function/macro: the "assist" target isn't updated fast enough.
* The macro "/startattack" will always initiate auto-attack (or auto-shot for hunters, if the appropriate interface option is active).

==Patch changes==
* {{Patch 2.0.1|note=Protected}}
```