# API C PetJournal.PetIsSlotted

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether a battle pet in your collection is part of your current battle pet team.
 isSlotted = C_PetJournal.PetIsSlotted(petID)

==Arguments==
:;petID:{{apitype|string}} - GUID of a battle pet in your collection.

==Returns==
:;isSlotted:{{apitype|boolean}} - true if the battle pet is part of your current team (loadout), false otherwise.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```