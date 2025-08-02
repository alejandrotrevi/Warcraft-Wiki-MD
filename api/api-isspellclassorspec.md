# API IsSpellClassOrSpec

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether a given spell is specific to a specialization and/or class.
 spec, class = IsSpellClassOrSpec(spellName)
               IsSpellClassOrSpec(spellIndex, bookType)

==Arguments==
:;spellName:{{apitype|string}} - name of the spell currently known by the player.
----
:;spellIndex:{{apitype|number}} - spell book slot index, ascending from 1.
:;bookType:{{apitype|string}} - spell book type, e.g. BOOKTYPE_SPELL ("spell") for player's spell book.

==Returns==
:;spec:{{apitype|string?}} - name of the specialization the spell is exclusive to, nil if not a specialization-granted spell.
:;class:{{apitype|string}} - name of the class the spell is exclusive to, nil if not a class ability.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

<!-- luals
---@param spellName string
---@return string? spec
---@return string class
---@overload fun(spellIndex: number, bookType: string)
function IsSpellClassOrSpec(spellName) end
-->
```