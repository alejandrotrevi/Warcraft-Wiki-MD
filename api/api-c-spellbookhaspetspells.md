# API C SpellBook.HasPetSpells

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns the number of available abilities for the player's combat pet.
 numPetSpells, petNameToken = C_SpellBook.HasPetSpells()

==Returns==
:;numPetSpells:{{apitype|number}} - The number of pet abilities available, or nil if you do not have a pet with a spell book.
:;petNameToken:{{apitype|string}} - Pet type, can be "DEMON" or "PET".

==Details==
* This <code>numSpells</code> return value is ''not'' the number that are on the pet bar, but the number of entries in the pet's spell book.

==Patch changes==
* {{Patch 11.0.0|note=Added, replacement for {{api|HasPetSpells}}.}}
```