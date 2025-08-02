# API C PetJournal.GetPetAbilityList

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns pet battle abilities available to a particular battle pet species.
 idTable, levelTable = C_PetJournal.GetPetAbilityList(speciesID [, idTable, levelTable])

==Arguments==
:;speciesID:{{apitype|number}} : [[BattlePetSpeciesID]] - Battle pet species ID to query the abilities of.
:;idTable:{{apitype|table?}} - Table that will be used to return ability ID information; a new table will be created if this argument is omitted.
:;levelTable:{{apitype|table?}}- Table that will be used to return ability level requirement information; a new table will be created if this argument is omitted.

==Returns==
:;idTable:{{apitype|number[]}} - An array of ability IDs available to the battle pet species.
:;levelTable:{{apitype|number[]}} - An array of levels at which the corresponding ability in the <code>idTable</code> becomes available to the species.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetAbilityInfoByID}} - Get information about a pet ability when you already know its abilityID
* {{api|C_PetJournal.GetPetAbilityInfo}} - Get information about a pet ability when you only know the pet and slot
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```