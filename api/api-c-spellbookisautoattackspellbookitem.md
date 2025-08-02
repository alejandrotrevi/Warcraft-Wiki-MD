# API C SpellBook.IsAutoAttackSpellBookItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns true if the SpellBookItem is the player's melee Auto Attack spell
 isAutoAttack = C_SpellBook.IsAutoAttackSpellBookItem(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;isAutoAttack:{{apitype|boolean}}
```