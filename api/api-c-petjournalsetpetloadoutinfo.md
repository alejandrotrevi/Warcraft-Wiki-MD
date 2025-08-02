# API C PetJournal.SetPetLoadOutInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Places the specified pet into a battle pet slot.
 C_PetJournal.SetPetLoadOutInfo(slotIndex, petID)

==Arguments==
:;slotIndex:{{apitype|number}} - Battle pet slot index, integer between 1 and 3.
:;petID:{{apitype|string}} - Battle pet GUID of a pet in your collection to move into the battle pet slot.

==Details==
* If the pet specified by <code>petID</code> is already in a battle pet slot, the pets are exchanged.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetJournal.SetAbility}}
* {{api|C_PetJournal.GetPetLoadOutInfo}}
```