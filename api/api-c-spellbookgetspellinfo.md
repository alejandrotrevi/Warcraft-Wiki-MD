# API C SpellBook.GetSpellInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Needs summary.
 spellInfo = C_SpellBook.GetSpellInfo(spellID)

==Arguments==
:;spellID:{{apitype|number}}

==Returns==
:;spellInfo:{{apitype|SpellInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| iconID || {{apitype|number}} || 
|-
| castTime || {{apitype|number}} || 
|-
| minRange || {{apitype|number}} || 
|-
| maxRange || {{apitype|number}} || 
|-
| spellID || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 11.0.0|note=Removed, replaced by {{api|C_Spell.GetSpellInfo}}.}}
* {{Patch 9.1.0|note=Added.}}
```