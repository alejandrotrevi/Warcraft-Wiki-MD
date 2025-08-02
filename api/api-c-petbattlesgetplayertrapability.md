# API C PetBattles.GetPlayerTrapAbility

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the ability ID for the best trap available to the player in the pet battle.
 trapAbilityID = C_PetBattles.GetPlayerTrapAbility()

==Returns==
:;trapAbilityID:{{apitype|number}} - Ability ID of the best trap you have available.

==Details==
Additional and better traps unlock through achievements, and this function will give different returns as those achievements are accomplished.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.IsTrapAvailable}} - Determine if trap can be used
* {{api|C_PetBattles.UseTrap}} - Attempt to trap the opponent
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```