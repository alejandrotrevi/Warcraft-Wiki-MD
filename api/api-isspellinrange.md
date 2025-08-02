# API IsSpellInRange

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns 1 if the player is in range to use the specified spell on the target unit, 0 otherwise.
 inRange = IsSpellInRange(spellName, unit)
         = IsSpellInRange(index, bookType, unit)

==Arguments==
:;spellName:{{apitype|string}} - The localized spell name. The player must know the spell.
:;unit:{{apitype|string}} : [[UnitId]] - The unit to use as a target for the spell.

{| class="darktable mw-collapsible mw-collapsed"
! Spellbook args &nbsp;
|-
|
:;index:{{apitype|number}} - Spellbook slot index, ranging from 1 through the [[API GetSpellTabInfo|total number]] of spells across all tabs and pages.
:;bookType:{{apitype|string}} - <code>BOOKTYPE_SPELL</code> or <code>BOOKTYPE_PET</code> depending on if you wish to query the player or pet spellbook.
:::<small>Internally the game only tests if this is equal to <code>"pet"</code> and treats any other string value as "spell".</small>
{{:Const_BOOKTYPE}}
|}

==Returns==
:;inRange:{{apitype|number?}} - <code>1</code> if the target is in range of the spell, <code>0</code> if the target is not in range of the spell, <code>nil</code> if the provided arguments were invalid or inapplicable.

==Details==
* This takes into account talents, and can be used to determine the approximate distance to your raid members.
* The function returns <code>nil</code> if:
** The spell cannot be cast on the unit. i.e. [[Frostbolt]] on a friendly unit, or [[Heal]] on an hostile unit (such as a mind-controlled raid member)
** If the unit is not 'visible' (per {{api|UnitIsVisible}}) or does not exist (per {{api|UnitExists}})
** The current player does not know this spell (so you cannot use 'Heal' to test 40 yard range for anyone other than a priest)
** The spell can only be cast on the player (i.e. a self-buff such as [[Mage Armor]] or [[Barkskin]])

==Example==
<syntaxhighlight lang="lua">
if IsSpellInRange("Flash Heal", "target") == 1 then
    print("target is in healing range")
else
    print("cannot heal target")
end
</syntaxhighlight>
<!-- luacats
---@param spellName string
---@param unit UnitId
---@return number? inRange
---@overload fun(index: number, bookType: string, unit: UnitId)
function IsSpellInRange(spellName, unit) end
-->
```