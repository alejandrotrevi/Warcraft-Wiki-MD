# API C PetBattles.IsInBattle

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether or not there is a pet battle in progress.
 inBattle = C_PetBattles.IsInBattle()

==Returns==
:;inBattle:{{apitype|boolean}} - True if in a pet battle, false if not

==Details==
This function starts to return true when {{api|t=e|PET_BATTLE_OPENING_START}} fires. It returns false again after {{api|t=e|PET_BATTLE_OVER}} fires.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```