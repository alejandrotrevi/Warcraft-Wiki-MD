# API UnitBattlePetSpeciesID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the battle pet species ID of a specified unit.
 speciesID = UnitBattlePetSpeciesID(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit to return the species ID of.

==Returns==
:;speciesID:{{apitype|number}} : [[BattlePetSpeciesID]]

==See also==
* {{api|UnitIsBattlePet}}
* {{api|C_PetJournal.GetPetInfoBySpeciesID}}

==Patch changes==
* {{Patch 5.1.0|note=Added.}}
```