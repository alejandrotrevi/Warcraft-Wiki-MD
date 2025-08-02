# API C PetBattles.GetAbilityProcTurnIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the turn index for a specific ability and proc type.
 turnIndex = C_PetBattles.GetAbilityProcTurnIndex(abilityID, procType)

==Arguments==
:;abilityID:{{apitype|number}} - ID of the ability.
:;procType:{{apitype|number}} - Index corresponding to a proc type.

==Returns==
:;turnIndex:{{apitype|number}} - Number of rounds that the ability has been in play.

==Details==
Proc types are defined in FrameXML/Constants.lua. They are currently:
 PET_BATTLE_EVENT_ON_APPLY = 0;
 PET_BATTLE_EVENT_ON_DAMAGE_TAKEN = 1
 PET_BATTLE_EVENT_ON_DAMAGE_DEALT = 2
 PET_BATTLE_EVENT_ON_HEAL_TAKEN = 3
 PET_BATTLE_EVENT_ON_HEAL_DEALT = 4
 PET_BATTLE_EVENT_ON_AURA_REMOVED = 5
 PET_BATTLE_EVENT_ON_ROUND_START = 6
 PET_BATTLE_EVENT_ON_ROUND_END = 7
 PET_BATTLE_EVENT_ON_TURN = 8
 PET_BATTLE_EVENT_ON_ABILITY = 9
 PET_BATTLE_EVENT_ON_SWAP_IN = 10
 PET_BATTLE_EVENT_ON_SWAP_OUT = 11

Since there are only 12 possible values for procType, you can usually afford to just do a loop such as <code>for procType = 0, 11 do</code> instead of finding out the actual procType.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetAbilityEffectInfo}} - the only known use for turnIndex is in this function
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```