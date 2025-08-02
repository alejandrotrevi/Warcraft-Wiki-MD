# API C PetBattles.GetSelectedAction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the selected action of a specific pet in the pet battle.
 selectedActionType, selectedActionIndex = C_PetBattles.GetSelectedAction()

==Returns==
:;selectedActionType:{{apitype|number}} - 2: Ability, 3: Switch Pet, 4: Trap, 5: Skip turn
:;selectedActionIndex:{{apitype|number}} - Returned values are 1-3, corresponding to the ability buttons from left to right.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.SkipTurn}} - Use an ability
* {{api|C_PetBattles.UseTrap}} - Use your trap
* {{api|C_PetBattles.ChangePet}} - Change your pet
* {{api|C_PetBattles.SkipTurn}} - Skip your turn


* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```