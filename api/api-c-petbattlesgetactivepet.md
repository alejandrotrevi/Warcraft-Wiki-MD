# API C PetBattles.GetActivePet

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index of the active pet for the specified owner in the pet battle.
 petIndex = C_PetBattles.GetActivePet(petOwner)

==Arguments==
:;petOwner:{{apitype|number}} - 1: Current player, 2: Opponent

==Returns==
:;petIndex:{{apitype|number}} - Returned values are always 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.ChangePet}} - Change to another pet
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```