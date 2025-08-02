# API UnitAttackBothHands

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the unit's melee attacks.
 mainBase, mainMod, offBase, offMod = UnitAttackBothHands(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - Tested with <code>"player"</code> and <code>"target"</code>.

==Returns==
:;mainBase:{{apitype|number}} - The unit's base main hand weapon skill (not rating).
:;mainMod:{{apitype|number}} - Any modifier to the unit's main hand weapon skill (not rating).
:;offBase:{{apitype|number}} - The unit's base offhand weapon skill (not rating)(equal to unarmed weapon skill if unit doesn't dual wield).
:;offMod:{{apitype|number}} - Any modifier to the unit's offhand weapon skill (not rating).
```