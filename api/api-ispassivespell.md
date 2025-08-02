# API IsPassiveSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the specified spell is a passive ability.
 isPassive = IsPassiveSpell(spellId or index, bookType)

==Arguments==
:;spellId:{{apitype|number}} - spell ID to query.

:;index:{{apitype|number}} - spellbook slot index, ascending from 1.
:;bookType:{{apitype|string}} - Either '''BOOKTYPE_SPELL''' ("spell") or '''BOOKTYPE_PET''' ("pet"). "spell" is linked to your General Spellbook tab.


==Returns==
:;isPassive:Flag : 1 if the spell is passive, nil otherwise.

==Details==
: With my Human Paladin, here are the "spells" I found to be Passive:
:: Block (Passive)
:: Diplomacy (Racial Passive)
:: Dodge (Passive)
:: Mace Specialization (Passive)
:: Parry (Passive)
:: Sword Specialization (Passive)
:: The Human Spirit  (Racial Passive)
```