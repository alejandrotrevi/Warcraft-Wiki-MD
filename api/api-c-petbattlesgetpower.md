# API C PetBattles.GetPower

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current Power of a specific pet in the pet battle.
 power = C_PetBattles.GetPower(petOwner, petIndex)

==Arguments==
:;petOwner:{{apitype|number}} - 1: Current player, 2: Opponent
:;petIndex:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.

==Returns==
:;power:{{apitype|number}} - Current amount of Power that the pet has

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetSpeed}} - Get speed of a specific pet
* {{api|C_PetBattles.GetMaxHealth}} - Get maximum health of a specific pet
* {{api|C_PetBattles.GetHealth}} - Get current health of a specific pet
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```