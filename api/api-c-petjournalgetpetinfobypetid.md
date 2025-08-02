# API C PetJournal.GetPetInfoByPetID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a battle pet.
 speciesID, customName, level, xp, maxXp, displayID, isFavorite, name, icon, petType, creatureID, sourceText, description, isWild, canBattle, isTradeable, isUnique, obtainable = C_PetJournal.GetPetInfoByPetID(petID)

==Arguments==
:;petID:{{apitype|string}} : [[GUID#BattlePet|GUID]]

==Returns==
{| class="darktable zebra col1-center"
! Index !! Value !! Type !! Details
|-
| 1 || speciesID || {{apitype|number}} || [[BattlePetSpeciesID]]
|-
| 2 || customName || {{apitype|string}} || Name assigned by the player or nil if unnamed
|-
| 3 || level || {{apitype|number}} || The pet's current battle level
|-
| 4 || xp || {{apitype|number}} || The pet's current xp
|-
| 5 || maxXp || {{apitype|number}} || The pet's maximum xp
|-
| 6 || displayID || {{apitype|number}} || The [[CreatureDisplayID|display ID]] of the pet
|-
| 7 || isFavorite || {{apitype|boolean}} || Whether the pet is marked as a favorite
|-
| 8 || name || {{apitype|string}} || Name of the pet species ("Albino Snake", "Blue Mini Jouster", etc.)
|-
| 9 || icon || {{apitype|fileID}} || Full path for the species' icon
|-
| 10 || petType || {{apitype|number}} || Index of the species' pet type
|-
| 11 || creatureID || {{apitype|number}} || NPC ID for the summoned companion pet
|-
| 12 || sourceText || {{apitype|string}} || Section of the tooltip that provides location information
|-
| 13 || description || {{apitype|string}} || Section of the tooltip that provides pet description ("flavor text")
|-
| 14 || isWild || {{apitype|boolean}} || For pets in the player's possession, true if the pet ''was'' caught in the wild. For pets not in the player's possession, true if the pet ''can'' be caught in the wild.
|-
| 15 || canBattle || {{apitype|boolean}} || True if this pet can be used in battles, false otherwise.
|-
| 16 || isTradeable || {{apitype|boolean}} || True if this pet can be traded, false otherwise.
|-
| 17 || isUnique || {{apitype|boolean}} || True if this pet is unique, false otherwise.
|-
| 18 || obtainable || {{apitype|boolean}} || True if this pet can be obtained, false otherwise (only false for tamer pets and developer/test pets).
|}

==Details==
* Information about the player's battle pets is available after {{api|t=e|UPDATE_SUMMONPETS_ACTION}} has fired.

==Patch changes==
* {{Patch 5.2.0|note=Added 18th return value, "obtainable".}}
* {{Patch 5.1.0|note=Added isFavorite return value.}}
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetJournal.GetPetStats}}
* {{api|C_PetJournal.GetPetInfoBySpeciesID}}

<!-- luals
---@param petID string
---@return number speciesID
---@return string customName
---@return number level
---@return number xp
---@return number maxXp
---@return number displayID
---@return boolean favorite
---@return string name
---@return fileID icon
---@return number petType
---@return string creatureID
---@return string sourceText
---@return string description
---@return boolean isWild
---@return boolean canBattle
---@return boolean isTradeable
---@return boolean isUnique
---@return boolean obtainable
function C_PetJournal.GetPetInfoByPetID(petID) end
-->
```