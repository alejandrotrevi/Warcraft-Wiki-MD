# API C PetJournal.SummonPetByGUID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 5.1}}
Summons (or dismisses) a pet.
 C_PetJournal.SummonPetByGUID(petID)

==Arguments==
:;petID:{{apitype|string}} - GUID of the battle pet to summon. If the pet is already summoned, it will be dismissed.

==Details==
You can dismiss the currently-summoned battle pet by running
 C_PetJournal.SummonPetByGUID(C_PetJournal.GetSummonedPetGUID())
Note that this will throw an error if you do not have a pet summoned.

Blizzard has moved all petIDs over to the "petGUID" system, but left all of their functions using the petID terminology (not the petGUID terminology) except for this one. For consistency, the term "petID" should continue to be used.

==Patch changes==
* {{Patch 5.1.0|note=Changed to <code>C_PetJournal.SummonPetByGUID()</code>, the first argument is now a GUID string.|comment=The GUID can be derived from the old (numeric) unique pet IDs using <code>petGUID = ("0x%016x"):format(petID)</code>.}}
* {{Patch 5.0.4|note=Added as <code>C_PetJournal.SummonPetByID()</code>}}

==See Also==
* {{api|C_PetJournal.GetSummonedPetGUID}}
```