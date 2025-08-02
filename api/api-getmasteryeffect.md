# API GetMasteryEffect

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the effective mastery percentage.
 masteryEffect, bonusCoefficient = GetMasteryEffect()

==Returns==
:;masteryEffect:{{apitype|number}} - Current effect of the player's mastery, typically a damage increase percentage, or a percentage chance to trigger some specialization-specific effect.
:;bonusCoefficient:{{apitype|number}} - A spec-dependent coefficient multiplied onto the player's raw mastery effect (as returned by {{api|GetMastery}}) to yield the actual effect of the mastery.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```