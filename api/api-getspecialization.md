# API GetSpecialization

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|future=1|patch=11.2.0|link=https://github.com/Gethe/wow-ui-source/blob/11.2.0/Interface/AddOns/Blizzard_DeprecatedSpecialization/Deprecated_Specialization_Standard.lua#L15-L16}}
Returns the index of the player's current specialization.
 currentSpec = GetSpecialization([isInspect [, isPet [, specGroup]]])

==Arguments==
:;isInspect:{{apitype|boolean?}} - if true, return information for the inspected player
:;isPet:{{apitype|boolean?}} - if true, return information for the player's pet.
:;specGroup:{{apitype|number?}} - The index of a given specialization/talent/glyph group (1 for primary / 2 for secondary).

==Returns==
:;currentSpec:{{apitype|number}} - index of the current specialization (ascending from 1), or nil if no specialization is currently learned.

==Example==
The following snippet prints the name of the player's current specialization if you have one selected.
 local currentSpec = GetSpecialization()
 if currentSpec then
    local _, currentSpecName = GetSpecializationInfo(currentSpec)
    print("Your current spec:", currentSpecName)
 else
    print("You do not currently have a spec.")
 end

==Details==
* For inspecting another player's spec, see {{api|GetInspectSpecialization}}()
* Returns a value of 5 as of 9.0.1 for newly created characters.
{| {{apitable}}
{{apirow | Related API | {{api|GetSpecializationInfo}} }}
{{apirow | Related Events | {{api|t=e|PLAYER_SPECIALIZATION_CHANGED}} }}
|}

==Patch changes==
* {{Patch 5.0.4|note=Replaced {{api|GetPrimaryTalentTree}}.}}
```