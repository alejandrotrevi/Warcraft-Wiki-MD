# API C PetBattles.GetAbilityEffectInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the effect info for a pet's ability.
 value = C_PetBattles.GetAbilityEffectInfo(abilityID, turnIndex, effectIndex, effectName)

==Arguments==
:;abilityID:{{apitype|number}} - The ID of this ability.
:;turnIndex:{{apitype|number}} - The turn in question for this ability. This can be obtained from {{api|C_PetBattles.GetAbilityProcTurnIndex}}.
:;effectIndex:{{apitype|number}} - The effect in question for this ability. This can be obtained from the unparsed description for this ability with extensive string manipulation, but currently no ability has more than 7 effects, so loops work too.
:;effectName:{{apitype|string}} - One of the effect names from {{api|C_PetBattles.GetAllEffectNames}}.

==Returns==
:;value:{{apitype|number}} - The information you requested for a specific element of a certain effect of a certain ability at a specific turn.

==Remarks==

To return the damage '''variance''' of [[Baby Winston|Baby Winston's]] [[Tesla Cannon]]:

 /dump C_PetBattles.GetAbilityEffectInfo(1625, 1, 1, "variance")
 [1]=60

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetAbilityProcTurnIndex}} - can be used to obtain the turnIndex for procs
* {{api|C_PetBattles.GetAllEffectNames}} - generates a list of all effectNames currently in the game
* {{api|C_PetBattles.GetAbilityInfo}} - return common general ability information
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```