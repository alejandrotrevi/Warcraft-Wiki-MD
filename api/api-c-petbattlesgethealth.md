# API C PetBattles.GetHealth

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current health of a specific pet in the current pet battle.
 health = C_PetBattles.GetHealth(petOwner, petIndex)

==Arguments==
:;petOwner:{{apitype|number}} - 1: Current player, 2: Opponent
:;petIndex:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.

==Returns==
:;health:{{apitype|number}} - Current health amount of the pet

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetMaxHealth}} - Get maximum health of a specific pet
* {{api|C_PetBattles.GetSpeed}} - Get speed of a specific pet
* {{api|C_PetBattles.GetPower}} - Get power of a specific pet
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```