# API C SpellBook.GetSpellBookItemCooldown

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns the cooldown info of a spell.
 spellCooldownInfo = C_SpellBook.GetSpellBookItemCooldown(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}} - Spellbook slot index, ranging from 1 through the total number of spells across all tabs and pages
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;spellCooldownInfo:{{apitype|SpellCooldownInfo?}} - Returns nil if item doesn't exist or if this kind of item doesn't display cooldowns (ex: future or offspec spells)
{{:Struct SpellCooldownInfo|nocaption=1}}

==Details==
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|SPELL_UPDATE_COOLDOWN}} }}
|}

==Patch changes==
* {{Patch 11.0.0|note=Added, replacement for {{api|GetSpellCooldown}}.}}
```