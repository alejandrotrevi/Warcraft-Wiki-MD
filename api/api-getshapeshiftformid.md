# API GetShapeshiftFormID

**Contributor:** JSON135

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the ID of the form or stance the player is currently in.
 index = GetShapeshiftFormID()

==Returns==
:;index:{{apitype|number}} - one of following:
::;All:
:::* nil = humanoid form

::;{{text|druid|Druid}}:
:::* Aquatic Form - 4
:::* Bear Form - 5 (BEAR_FORM constant)
:::* Cat Form - 1 (CAT_FORM constant)
:::* Flight Form - 29
:::* Moonkin Form - 31 - 35 (MOONKIN_FORM constant) (different races seem to have different numbers)
:::* Swift Flight Form - 27
:::* Travel Form - 3
:::* Tree of Life - 2
:::* Treant Form - 36

::;{{text|monk|Monk}} {{mop-inline}}:
:::* Stance of the Fierce Tiger - 24
:::* Stance of the Sturdy Ox - 23
:::* Stance of the Wise Serpent - 20

::;{{text|rogue|Rogue}}:
:::* Stealth - 30

::;{{text|shaman|Shaman}}:
:::* Ghost Wolf - 16

::;{{text|warlock|Warlock}}:
:::* Metamorphosis - 22

::;{{text|warrior|Warrior}}:
:::* Battle Stance - 17
:::* Berserker Stance - 19
:::* Defensive Stance - 18

==Details==
Similar to the function [[API GetShapeshiftForm|GetShapeshiftForm]](flag), except the values returned are constant and not dependent on forms available to the unit or current class.
```