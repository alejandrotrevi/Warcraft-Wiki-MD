# API C SpellBook.GetSpellBookItemLossOfControlCooldown

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns nil if item doesn't exist or if this kind of item doesn't display cooldowns (ex: future or offspec spells)
 startTime, duration = C_SpellBook.GetSpellBookItemLossOfControlCooldown(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;startTime:{{apitype|number}}
:;duration:{{apitype|number}}
```