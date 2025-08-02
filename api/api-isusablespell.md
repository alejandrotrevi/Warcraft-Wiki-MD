# API IsUsableSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.0.0|removed=11.0.2}}
Determines whether a spell can be used by the player character.
 usable, noMana = IsUsableSpell(spell)
                = IsUsableSpell(index, bookType)

==Arguments==
{{:SpellArg}}

==Returns==
:;usable:{{apitype|boolean}} - True if the spell is usable, false otherwise. A spell might be un-usable for a variety of reasons, such as:
:* The player hasn't learned the spell
:* The player lacks required mana or reagents.
:* Reactive conditions haven't been met.
:;noMana:{{apitype|boolean}} - True if the spell can not be cast due to low mana, false otherwise.

==Example==
The following code snippet will check if the spell 'Healing Touch' can be cast:
  usable, nomana = IsUsableSpell("Curse of Elements");
  if (not usable) then
   if (not nomana) then
     message("The spell cannot be cast");
   else
     message("You do not have enough mana to cast the spell");
   end
  else
     message("The spell may be cast");
  end
The following code snippet will check if the 20th spell in the player's spellbook is usable:
  usable, nomana = IsUsableSpell(20, BOOKTYPE_SPELL); 
  print(GetSpellName(20, BOOKTYPE_SPELL) .. " is " .. (usable and "" or "not ") .. " usable.");

==Patch changes==
* {{Patch 11.0.0|note=Removed, replaced by {{api|C_Spell.IsSpellUsable}} and {{api|C_SpellBook.IsSpellBookItemUsable}}.}}
```