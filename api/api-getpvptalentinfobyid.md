# API GetPvpTalentInfoByID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a PvP (honor) talent.
 talentID, name, icon, selected, available, spellID, unlocked, row, column, known, grantedByAura = GetPvpTalentInfoByID(talentID [, specGroupIndex, isInspect, inspectedUnit])

==Arguments==
:;talentID:{{apitype|number}} - Talent ID.
:;specGroupIndex:{{apitype|number?}} - Index of active specialization group ({{api|GetActiveSpecGroup}}); if nil, the selected/available return values will always be false.
:;isInspect:{{apitype|boolean?}} - If non-nil, returns information based on inspectedUnit.
:;inspectedUnit:{{apitype|string?}} - Inspected [[unitId]].

==Returns==
:;1. talentID:{{apitype|number}} - Talent ID.
:;2. name:{{apitype|string}} - Talent name.
:;3. icon:{{apitype|number}} - [[FileID]]
:;4. selected:{{apitype|boolean}} - true if the talent is chosen, false otherwise.
:;5. available:{{apitype|boolean}} - true if the talent tier is chosen, or if it is level-appropriate for the player and the player has no talents selected in that tier, false otherwise.
:;6. spellID:{{apitype|number}} - Spell ID that is added to the spellbook.
:;7. unlocked:{{apitype|boolean}} - Whether the talent is unlocked.
:;8. row:{{apitype|number}} - The row the talent is from.
:;9. column:{{apitype|number}} - The column the talent is from.
:;10. known:{{apitype|boolean}} - true if the talent is known, false otherwise.
:;11. grantedByAura:{{apitype|boolean}} - true if the talent is granted by an aura (i.e., an effect on an item), false otherwise. The [[Conflict and Strife]] [[Azerite Essence]] uses this instead of selected.

==Patch changes==
* {{Patch 8.0.1|note=PvP talents are no longer organized into a row/column table.}}

==See also==
* {{api|GetTalentInfo}}
```