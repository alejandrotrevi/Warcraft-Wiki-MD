# API C PetBattles.GetAuraInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information for an aura in a pet battle.
 auraID, instanceID, turnsRemaining, isBuff = C_PetBattles.GetAuraInfo(petOwner, petIndex, auraIndex)

==Arguments==
:;petOwner:{{apitype|number}} - 1: Current player, 2: Opponent.
:;petIndex:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.
:;auraIndex:{{apitype|number}} - The number from an index of all active auras.

==Returns==
:;auraID:{{apitype|number}} - The ability ID of the aura (all auras are abilities too).
:;instanceID:{{apitype|number}} - A unique identifier for this aura; used for differentiation purposes only.
:;turnsRemaining:{{apitype|number}} - The number of rounds left for the aura to remain active.
:;isBuff:{{apitype|boolean}} - True if the aura is displayed to the user, false otherwise.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetNumAuras}} - use this function to get the maximum index of the active auras
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```