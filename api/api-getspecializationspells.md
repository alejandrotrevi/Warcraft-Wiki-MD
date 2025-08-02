# API GetSpecializationSpells

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the spells learned as part of the specified specialization.
 spellID1, level1, spellID2, level2, ... = GetSpecializationSpells(specIndex [, isInspect, isPet])

==Arguments==
:;specIndex:{{apitype|number}} - index of the specialization to query, integer ascending from 1.
:;isInspect:{{apitype|boolean?}} - a truthy value to query information about the inspected unit; player information is returned otherwise.
:;isPet:{{apitype|boolean?}} - a truthy value to query information about a pet specialization; player information is returned otherwise.

==Returns==
An unsorted list of (spellID, level) pairs:
:;spellID:{{apitype|number}} - spell learned as part of the specialization.
:;level:{{apitype|number}} - level at which the spell is learned by the specialization.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|GetSpecsForSpell}}

<!-- luals
---@param specIndex number
---@param isInspect? boolean
---@param isPet? boolean
---@return number spellID
---@return number level
---@return number ...
function GetSpecializationSpells(specIndex, isInspect, isPet) end
-->
```