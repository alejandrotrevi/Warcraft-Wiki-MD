# API C PetJournal.FindPetIDByName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns pet species and GUID by pet name.
 speciesId, petGUID = C_PetJournal.FindPetIDByName(petName)

==Arguments==
:;petName:{{apitype|string}} - Name of the pet to find species/GUID of.

==Returns==
:;speciesId:{{apitype|number}} - Species ID of the first battle pet (or species) with the specified name, nil if no such pet exists.
:;petGUID:{{apitype|string}} - GUID of the first battle pet collected by the player with the specified name, nil if the player has not collected any pets with the specified name.

==Patch changes==
* {{Patch 5.1.0|note=Added.}}
```