# API HasPetSpells

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of available abilities for the player's combat pet.
 numSpells, petToken = HasPetSpells()

==Returns==
:;numSpells:{{apitype|number}} - The number of pet abilities available, or nil if you do not have a pet with a spell book.
:;petToken:{{apitype|string}} - Pet type, can be "DEMON" or "PET".

==Description==
* This <code>numSpells</code> return value is ''not'' the number that are on the pet bar, but the number of entries in the pet's spell book.

==Patch changes==
* {{Patch 11.0.0|note=Removed, replaced by {{api|C_SpellBook.HasPetSpells}}.}}
```