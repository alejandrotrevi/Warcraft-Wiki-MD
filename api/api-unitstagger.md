# API UnitStagger

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the amount of staggered damage on the unit.
 damage = UnitStagger(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;damage:{{apitype|number}} - current amount of staggered damage on the unit.

==Details==
* [[Stagger]] allows [[monk]]s to spread a fraction of incoming damage over the next 10 seconds. This function returns the total amount of damage Stagger will cause the monk to take over the next 10 seconds.

==Patch changes==
* {{Patch 5.2.0|note=Added.}}
```