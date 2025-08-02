# API C PetBattles.GetNumAuras

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of active auras affecting the current pet in the pet battle.
 numAuras = C_PetBattles.GetNumAuras(petOwner, petIndex)

==Arguments==
:;petOwner:{{apitype|number}} - 1: Current player, 2: Opponent.
:;petIndex:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.

==Returns==
:;numAuras:{{apitype|number}} - Amount of active auras affecting the pet.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetAuraInfo}} - the only use for the number of auras is to figure out the largest auraIndex that GetAuraInfo will accept
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```