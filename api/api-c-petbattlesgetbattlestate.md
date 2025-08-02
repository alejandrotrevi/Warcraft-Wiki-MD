# API C PetBattles.GetBattleState

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current battle state for the pet battle.
 battleState = C_PetBattles.GetBattleState()

==Returns==
:;battleState:{{apitype|number}} - A value representing the state of the battle.

==Details==
Note that the constants for battle states are not defined in FrameXML. Here are the currently known ones:
 LE_PET_BATTLE_STATE_CREATED = 1
 LE_PET_BATTLE_STATE_WAITING_PRE_BATTLE = 2
 LE_PET_BATTLE_STATE_ROUND_IN_PROGRESS = 3
 LE_PET_BATTLE_STATE_WAITING_FOR_ROUND_PLAYBACK = 4
 LE_PET_BATTLE_STATE_WAITING_FOR_FRONT_PETS = 5
 LE_PET_BATTLE_STATE_CREATED_FAILED = 6
 LE_PET_BATTLE_STATE_FINAL_ROUND = 7
 LE_PET_BATTLE_STATE_FINISHED = 8

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```