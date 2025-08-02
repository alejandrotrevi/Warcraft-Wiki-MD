# API UnitSelectionColor

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the color of the outline and circle underneath the unit.
 red, green, blue, alpha = UnitSelectionColor(unit [, useExtendedColors])

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit whose selection colour should be returned.
:;useExtendedColors:{{apitype|boolean?|default=false}} - If true, a more appropriate colour of the unit's selection will be returned. For instance, if used on a dead hostile target, the default return will red (hostile), but the extended return will be grey (dead).

==Returns==
:;red:{{apitype|number}} - A number between 0 and 1.
:;green:{{apitype|number}} - A number between 0 and 1.
:;blue:{{apitype|number}} - A number between 0 and 1.
:;alpha:{{apitype|number}} - A number between 0 and 1.

==Example==
 0, 0, 0.99999779462814, 0.99999779462814 = UnitSelectionColor("player")
 0, 0.99999779462814, 0, 0.99999779462814 = UnitSelectionColor("target") -- a friendly npc in target

==See Also==
* [[API UnitSelectionType]]
```