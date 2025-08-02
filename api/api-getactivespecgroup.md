# API GetActiveSpecGroup

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|future=1|patch=11.2.0|link=https://github.com/Gethe/wow-ui-source/blob/11.2.0/Interface/AddOns/Blizzard_DeprecatedSpecialization/Deprecated_Specialization_Standard.lua#L18-L19}}
Returns the index of the current active specialization/talent/glyph group.
 activeSpec = GetActiveSpecGroup([isInspect])

==Arguments==
:;isInspect:{{apitype|boolean?}} (Defaults to false) - If true returns the information for the inspected unit instead of the player.

==Returns==
:;activeSpec:{{apitype|number}} - The index of the player's active specialization/talent/glyph group (1 for primary / 2 for secondary).

==Patch changes==
* {{Patch 5.0.4|note=Replaced {{api|GetActiveTalentGroup}}.}}
```