# API C PetJournal.GetPetStats

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the stats of a collected battle pet.
 health, maxHealth, power, speed, rarity = C_PetJournal.GetPetStats(petID)

==Arguments==
:;petID:{{apitype|string}} - GUID of pet in Pet Journal (different than speciesID and displayID)

==Returns==
:;health:{{apitype|number}} - Current health of the pet. Zero or negative if the pet is dead.
:;maxHealth:{{apitype|number}} - Maximum health of the pet
:;power:{{apitype|number}}
:;speed:{{apitype|number}}
:;rarity:{{apitype|number}} - 1: "Poor", 2: "Common", 3: "Uncommon", 4: "Rare", 5: "Epic", 6: "Legendary"

==Details==
Use _G["BATTLE_PET_BREED_QUALITY"..rarity] to convert the rarity to a String while drawing on Blizzard's pre-existing localization information.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```