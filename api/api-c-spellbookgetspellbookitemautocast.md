# API C SpellBook.GetSpellBookItemAutoCast

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns nothing if item doesn't exist or isn't a spell
 autoCastAllowed, autoCastEnabled = C_SpellBook.GetSpellBookItemAutoCast(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;autoCastAllowed:{{apitype|boolean}} - True if this spell is allowed to be auto-cast
:;autoCastEnabled:{{apitype|boolean}} - True if auto-casting this spell is currently enabled (usually by the player)
```