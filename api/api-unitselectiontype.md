# API UnitSelectionType

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the selection type of the outline and circle underneath the unit.
 selectionType = UnitSelectionType(unit [, useExtendedColors])

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit whose selection type should be returned.
:;useExtendedColors:{{apitype|boolean?|default=false}} - If true, a more appropriate type of the unit's selection will be returned. For instance, if used on a dead hostile target, the default return will be 0 (hostile), but the extended return will be 9 (dead).

==Returns==
:;selectionType:{{apitype|number}} - The unit's selection type:
:::* 0 - Hostile.
:::* 1 - Unfriendly.
:::* 2 - Neutral.
:::* 3 - Friendly.
:::* 4 - Player.
:::* 5 - Player, if using extended colours.
:::* 6 - Party.
:::* 7 - Party (War Mode On).
:::* 8 - Friend, a player from your friend list.
:::* 9 - Dead.
:::* 10 - Commentator Team 1, only available to commentators.
:::* 11 - Commentator Team 2, only available to commentators.
:::* 12 - Self, your character if highlighting of your character is enabled.
:::* 13 - Friendly (Battleground), party members and friendly units in battlegrounds.

==Details==
* If the unit doesn't exist, this function will return 4 or 5, if using extended colours.

==Patch changes==
* {{Patch 8.1.5|note=Added.}}

==See also==
* [[API UnitSelectionColor]]
```