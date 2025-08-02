# API C PetBattles.GetAbilityStateModification

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the modification state for an ability.
 abilityStateMod = C_PetBattles.GetAbilityStateModification(abilityID, stateID)

==Arguments==
:;abilityID:{{apitype|number}} - ID of the ability.
:;stateID:{{apitype|number}} - ID of a state for Pet Battles.

==Returns==
:;abilityStateMod:{{apitype|number}} - The ability's modification state.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetAllStates}}
* {{api|C_PetBattles.GetStateValue}}
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```