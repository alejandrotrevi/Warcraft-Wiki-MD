# API C PetJournal.SetAbility

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Selects a battle pet ability to make available in battle.
 C_PetJournal.SetAbility(slotIndex, spellIndex, petSpellID)

==Arguments==
:;slotIndex:{{apitype|number}} - battle pet slot index, integer between 1 and 3.
:;spellIndex:{{apitype|number}} - ability slot index, integer between 1 and 3.
:;petSpellID:{{apitype|number}} - pet ability ID to select for the <code>spellIndex</code> slot of the pet in the <code>slotIndex</code> battle pet slot.

==Details==
* While this function allows you to select abilities outside of those specified by {{api|C_PetJournal.GetPetAbilityList}} (or assign those abilities to other ability slots), those abilities will not be usable in pet battles.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetJournal.GetPetLoadOutInfo}}
* {{api|C_PetJournal.GetPetAbilityList}}
* {{api|C_PetJournal.GetPetAbilityInfo}}
```