# API C PetJournal.GetSummonedPetGUID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a battle pet.
 summonedPetGUID = C_PetJournal.GetSummonedPetGUID()

==Returns==
:;summonedPetGUID:{{apitype|string}} - [[GUID#BattlePet|GUID]] identifying the currently-summoned battle pet, or nil if no battle pet is summoned.

==Details==
Blizzard has moved all petIDs over to the "petGUID" system, but left all of their functions using the petID terminology (not the petGUID terminology) except for this one. For consistency, the term "petID" should continue to be used.

==Patch changes==
* {{Patch 5.1.0|note=Changed to <code>C_PetJournal.GetSummonedPetGUID()</code>, the first argument is now a GUID string.|comment=The GUID can be derived from the old (numeric) unique pet IDs using <code>petGUID = ("0x%016x"):format(petID)</code>.}}
* {{Patch 5.0.4|note=Added (as <code>C_PetJournal.GetSummonedPetID()</code>).}}

==See Also==
* {{api|C_PetJournal.SummonPetByGUID}}
```