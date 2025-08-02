# API C PetBattles.ChangePet

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Changes the active pet out for a different pet in a pet battle.
 C_PetBattles.ChangePet(petIndex)

==Arguments==
:;petIndex:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.CanActivePetSwapOut}} - Tells you if the current pet can be swapped out
* {{api|C_PetBattles.CanPetSwapIn}} - Tells you if the specified pet can swapped in
* {{api|C_PetBattles.GetActivePet}} - Get the index of the current pet
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```