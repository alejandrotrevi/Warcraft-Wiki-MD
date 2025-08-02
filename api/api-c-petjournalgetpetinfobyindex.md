# API C PetJournal.GetPetInfoByIndex

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a battle pet.
 petID, speciesID, owned, customName, level, favorite, isRevoked, speciesName, icon, petType, companionID, tooltip, description, isWild, canBattle, isTradeable, isUnique, obtainable = C_PetJournal.GetPetInfoByIndex(index)

==Arguments==
:;index:{{apitype|number}} - Numeric index of the pet in the Pet Journal, ascending from 1.

==Returns==
{| class="darktable zebra col1-center"
! Index !! Value !! Type !! Details
|-
| 1 || petID || {{apitype|string}} || [[GUID#BattlePet|GUID]] for this specific pet
|-
| 2 || speciesID || {{apitype|number}} || [[BattlePetSpeciesID]]
|-
| 3 || owned || {{apitype|boolean}} || Whether the pet is owned by the player
|-
| 4 || customName || {{apitype|string}} || Name assigned by the player or nil if unnamed
|-
| 5 || level || {{apitype|number}} || The pet's current battle level
|-
| 6 || favorite || {{apitype|boolean}} || Whether the pet is marked as a favorite
|-
| 7 || isRevoked || {{apitype|boolean}} || True if the pet is {{api|C_PetJournal.PetIsRevoked|revoked}}; false otherwise.
|-
| 8 || speciesName || {{apitype|string}} || Name of the pet species ("Albino Snake", "Blue Mini Jouster", etc.)
|-
| 9 || icon || {{apitype|fileID}} || Full path for the species' icon
|-
| 10 || petType || {{apitype|number}} || Index of the species' petType.
|-
| 11 || companionID || {{apitype|number}} || NPC ID for the summoned companion pet.
|-
| 12 || tooltip || {{apitype|string}} || Section of the tooltip that provides location information
|-
| 13 || description || {{apitype|string}} || Section of the tooltip that provides pet description ("flavor text")
|-
| 14 || isWild || {{apitype|boolean}} || True if the pet was/can be caught in the wild, false otherwise.
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
*index is subject to filter and search result, eg a Search for "Snake" where index is 1 will return information about the first snake in journal where an empty search and filter will return information about first pet in journal.

==Patch changes==
* {{Patch 5.2.0|note=Added 18th return value, "obtainable". Removed "isWild" argument.}}
* {{Patch 5.0.4|note=Added.}}

<!-- luals
---@param index number
---@return string petID
---@return number speciesID
---@return boolean owned
---@return string customName
---@return number level
---@return boolean favorite
---@return boolean isRevoked
---@return string speciesName
---@return fileID icon
---@return number petType
---@return number companionID
---@return string tooltip
---@return string description
---@return boolean isWild
---@return boolean canBattle
---@return boolean isTradeable
---@return boolean isUnique
---@return boolean obtainable
function C_PetJournal.GetPetInfoByIndex(index) end
-->
```