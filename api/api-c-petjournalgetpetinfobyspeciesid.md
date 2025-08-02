# API C PetJournal.GetPetInfoBySpeciesID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a pet species.
 speciesName, speciesIcon, petType, companionID, tooltipSource, tooltipDescription, isWild, canBattle, isTradeable, isUnique, obtainable, creatureDisplayID = C_PetJournal.GetPetInfoBySpeciesID(speciesID)

==Arguments==
:;speciesID:{{apitype|number}} : [[BattlePetSpeciesID]]

==Returns==
{| class="darktable zebra col1-center"
! Index !! Value !! Type !! Details
|-
| 1 || speciesName || {{apitype|string}} || Name of the pet species ("Albino Snake", "Blue Mini Jouster", etc.)
|-
| 2 || speciesIcon || {{apitype|fileID}} || Full path for the species' icon
|-
| 3 || petType || {{apitype|number}} || [[BattlePetTypeID]]
|-
| 4 || companionID || {{apitype|number}} || NPC ID for the summoned companion pet.
|-
| 5 || tooltipSource || {{apitype|string}} || Section of the species tooltip that provides location information
|-
| 6 || tooltipDescription || {{apitype|string}} || Section of the species tooltip that provides pet description ("flavor text")
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
| 12 || creatureDisplayID || {{apitype|number}} || [[CreatureDisplayID|Creature display ID]] of the species.
|-
| 13 || desiredScale || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 6.0.2|note=Added 12th return value, "creatureDisplayID".}}
* {{Patch 5.2.0|note=Added 11th return value, "obtainable".}}
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetJournal.GetPetInfoByPetID}}

<!-- luals
---@param speciesID number
---@return string speciesName
---@return fileID speciesIcon
---@return number petType
---@return number companionID
---@return string tooltipSource
---@return string tooltipDescription
---@return boolean isWild
---@return boolean canBattle
---@return boolean isTradeable
---@return boolean isUnique
---@return boolean obtainable
---@return number creatureDisplayID
---@return number desiredScale
function C_PetJournal.GetPetInfoBySpeciesID(speciesID) end
-->
```