# API C PetJournal.GetPetInfoByItemID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves information about the battle pet species taught by the specified item.
 name, icon, petType, creatureID, sourceText, description, isWild, canBattle, isTradeable, isUnique, obtainable, displayID, speciesID = C_PetJournal.GetPetInfoByItemID(itemID)

==Arguments==
:;itemID:{{apitype|number}} - an item ID

==Returns==
{| class="darktable zebra col1-center"
! Index !! Value !! Type !! Details
|-
| 1 || name || {{apitype|string}} || Name of the pet species ("Albino Snake", "Blue Mini Jouster", etc.)
|-
| 2 || icon || {{apitype|fileID}} || Numeric identifier for the species' icon.
|-
| 3 || petType || {{apitype|number}} || [[BattlePetTypeID]]
|-
| 4 || creatureID || {{apitype|number}} || NPC ID for the summoned companion pet.
|-
| 5 || sourceText || {{apitype|string}} || Section of the species tooltip that provides location information.
|-
| 6 || description || {{apitype|string}} || Section of the species tooltip that provides pet description ("flavor text").
|-
| 7 || isWild || {{apitype|boolean}} || For pets in the player's possession, true if the pet ''was'' caught in the wild. For pets not in the player's possession, true if the pet ''can'' be caught in the wild.
|-
| 8 || canBattle || {{apitype|boolean}} || True if this pet can be used in battles, false otherwise.
|-
| 9 || isTradeable || {{apitype|boolean}} || True if this pet can be traded, false otherwise.
|-
| 10 || isUnique || {{apitype|boolean}} || True if this pet is unique, false otherwise.
|-
| 11 || obtainable || {{apitype|boolean}} || True if this pet can be obtained, false otherwise (only false for tamer pets and developer/test pets).
|-
| 12 || displayID || {{apitype|number}} || [[CreatureDisplayID]]
|-
| 13 || speciesID || {{apitype|number}} || [[BattlePetSpeciesID]]
|}

==Details==
* Unlike many other item-related API functions, this function ''only'' accepts an item ID; passing an item link will raise an error. However, the item ID may be a string rather than a number.

==Patch changes==
* {{Patch 8.1.0|note=Added.}}

==See also==
* {{api|C_PetJournal.GetPetInfoByIndex}}
* {{api|C_PetJournal.GetPetInfoByPetID}}
* {{api|C_PetJournal.GetPetInfoBySpeciesID}}

<!-- luals
---@param itemID number
---@return string name
---@return fileID icon
---@return number petType
---@return number creatureID
---@return string sourceText
---@return string description
---@return boolean isWild
---@return boolean canBattle
---@return boolean isTradeable
---@return boolean isUnique
---@return boolean obtainable
---@return number displayID
---@return number speciesID
function C_PetJournal.GetPetInfoByItemID(itemID) end
-->
```