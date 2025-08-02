# API GetTalentInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|future=1|patch=11.2.0|link=https://github.com/Gethe/wow-ui-source/blob/11.2.0/Interface/AddOns/Blizzard_DeprecatedSpecialization/Deprecated_Specialization_Standard.lua#L35-L51}} {{for|the {{Df-inline}} Dragonflight version|Dragonflight Talent System}} {{for|the {{Wotlk-inline}} Wrath version|API GetTalentInfo/Wrath}} {{for|the {{Wow-inline}} WoW Classic version|API GetTalentInfo/Classic}}
Returns info for the specified talent.
 talentID, name, texture, selected, available, spellID, unknown, row, column, known, grantedByAura
    = GetTalentInfo(tier, column, specGroupIndex [, isInspect, inspectUnit])
    = GetTalentInfoByID(talentID, specGroupIndex [, isInspect, inspectUnit])
    = GetTalentInfoBySpecialization(specIndex, tier, column)

==Arguments==
===<font color="#4ec9b0">GetTalentInfo</font>===
:;tier:{{apitype|number}} - Talent tier from 1 to <code>MAX_TALENT_TIERS</code>
:;column:{{apitype|number}} - Talent column from 1 to <code>NUM_TALENT_COLUMNS</code>
:;specGroupIndex:{{apitype|number}} - Index of active specialization group ({{api|GetActiveSpecGroup}})
:;isInspect:{{apitype|boolean?}} - If non-nil, returns information based on inspectedUnit/classId.
:;inspectUnit:{{apitype|string?}} : [[UnitId]] - Inspected unit; if nil, the selected/available return values will always be false.

===<font color="#4ec9b0">GetTalentInfoByID</font>===
:;talentID:{{apitype|number}} - Talent ID.
:;specGroupIndex:{{apitype|number}}
:;isInspect:{{apitype|boolean?}}
:;inspectUnit:{{apitype|string?}} : [[UnitId]]

===<font color="#4ec9b0">GetTalentInfoBySpecialization</font>===
:;specIndex:{{apitype|number}} - Index of the specialization, ascending from 1 to {{api|GetNumSpecializations}}().
:;tier:{{apitype|number}}
:;column:{{apitype|number}}

==Returns==
:;1. talentID:{{apitype|number}} - Talent ID.
:;2. name:{{apitype|string}} - Talent name.
:;3. texture:{{apitype|number}} : [[FileID]]
:;4. selected:{{apitype|boolean}} - true if the talent is chosen, false otherwise.
:;5. available:{{apitype|boolean}} - true if the talent tier is chosen, or if it is level-appropriate for the player and the player has no talents selected in that tier, false otherwise.
:;6. spellID:{{apitype|number}} - Spell ID that is added to the spellbook.
:;7. unknown:{{apitype|any}}
:;8. row:{{apitype|number}} - The row the talent is from.  This will be the same as the tier argument given.
:;9. column:{{apitype|number}} - The column the talent is from.  This will be the same as the column argument given.
:;10. known:{{apitype|boolean}} - true if the talent is active, false otherwise.
:;11. grantedByAura:{{apitype|boolean}} - true if the talent is granted by an aura (i.e., an effect on an item), false otherwise. Legion's Class Soul rings used this rather than selected.

==Patch changes==
* {{Patch 6.0.2|note=Changed params.}}
* {{Patch 5.0.4|note=Changed params.}}
<!-- luals
---@param tier number
---@param column number
---@param specGroupIndex? number
---@param isInspect? boolean
---@param inspectUnit? UnitToken
---@return number talentID
---@return string name
---@return number texture
---@return boolean selected
---@return boolean available
---@return number spellID
---@return any unknown
---@return number row
---@return number column
---@return boolean known
---@return boolean grantedByAura
function GetTalentInfo(tier, column, specGroupIndex, isInspect, inspectUnit) end

---[Documentation](https://warcraft.wiki.gg/wiki/API_GetTalentInfoByID)
---@param talentID number
---@param specGroupIndex number
---@param isInspect? boolean
---@param inspectUnit? UnitToken
---@return number talentID
---@return string name
---@return number texture
---@return boolean selected
---@return boolean available
---@return number spellID
---@return any unknown
---@return number row
---@return number column
---@return boolean known
---@return boolean grantedByAura
function GetTalentInfoByID(talentID, specGroupIndex, isInspect, inspectUnit) end

---[Documentation](https://warcraft.wiki.gg/wiki/API_GetTalentInfoBySpecialization)
---@param specIndex number
---@param tier number
---@param column number
---@return number talentID
---@return string name
---@return number texture
---@return boolean selected
---@return boolean available
---@return number spellID
---@return any unknown
---@return number row
---@return number column
---@return boolean known
---@return boolean grantedByAura
function GetTalentInfoBySpecialization(specIndex, tier, column) end
-->

==See also==
* {{api|IsPlayerSpell}}
* {{api|IsSpellKnown}}
```