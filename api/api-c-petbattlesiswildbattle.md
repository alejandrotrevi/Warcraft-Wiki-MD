# API C PetBattles.IsWildBattle

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether or not there is a wild pet battle in progress.
 inWildBattle = C_PetBattles.IsWildBattle()

==Returns==
:;inWildBattle:{{apitype|boolean}} - True if in a wild pet battle, false if not in a wild pet battle or not in a pet battle at all

==Details==
This function starts to return true when {{api|t=e|PET_BATTLE_OPENING_START}} fires if it is a wild battle. It returns false again after {{api|t=e|PET_BATTLE_OVER}} fires.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```