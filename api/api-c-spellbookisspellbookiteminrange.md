# API C SpellBook.IsSpellBookItemInRange

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns true if the current target is within range of the SpellBookIem; False if out of range; Nil if range check was invalid
 inRange = C_SpellBook.IsSpellBookItemInRange(spellBookItemSlotIndex, spellBookItemSpellBank [, targetUnit])

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}
:;targetUnit:{{apitype|UnitToken?}} - Optional specific target; If not supplied, player's current target (if any) will be used

==Returns==
:;inRange:{{apitype|boolean?}} - May be nil if the range check was invalid, ie due to unknown/invalid spell, missing/invalid target, etc
```