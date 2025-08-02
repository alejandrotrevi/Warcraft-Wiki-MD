# API C PetBattles.GetStateValue

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the value of a specific state for a specific pet in a pet battle.
 stateValue = C_PetBattles.GetStateValue(petOwner, petIndex, stateID)

==Arguments==
:;petOwner:{{apitype|number}} - Accepted values are actually 0 through 2, unlike all (?) other Pet Battle functions.
:;petIndex:{{apitype|number}} - Accepted values are actually 0 through 3, unlike all (?) other Pet Battle functions.
:;stateID:{{apitype|number}} - The ID of a Pet Battle's specific State.

==Returns==
:;stateValue:{{apitype|number}} - The value of the given state for the given pet.

==Details==
petOwner and petIndex can accept a value of zero in this function. A petOwner of "0" refers to the states controlled by the Game. For example, to check the weather state, you want to use a petOwner of "0" and a petIndex of "0" (which is the only valid petIndex for a petOwner of "0"). When petOwner is 1 (player) or 2 (enemy), setting the petIndex to "0" also works, but does something different - it refers to any objects (walls, barrels, bombs, mines, missile launchers, etc) or field effects currently in play for that team. For example, the DoT from [[Flamethrower]] is a field effect ("Turns the battlefield") that persists through pet swaps. To check the associated states, you need to set petOwner to 1 or 2 and petIndex to "0".

Note that some values corresponding to stateIDs do NOT update correctly. For example, stateID 78 "STATE_Stat_Gender" is always 0, regardless of petOwner, petIndex, or the pets in question. This suggests that Blizzard updates stateIDs on an individual basis and probably will not update any stateIDs that they do not actively use in Pet Battles at this time, such as those associated with Poison or Cloning.

==Example==
Here is an example of a possible use for stateIDs and state values. The following code is reverse engineered from Blizzard's own Battle Pet Ability tooltip parser.
 local AccuracyModifier
 	if (C_PetBattles.GetPetType(petOwner, petIndex) == 7) then -- Elementals aren't affected by weathers.
 		AccuracyModifier = C_PetBattles.GetStateValue(petOwner, petIndex, 41) + C_PetBattles.GetStateValue(petOwner, 0, 41)
 	else
 		AccuracyModifier = C_PetBattles.GetStateValue(petOwner, petIndex, 41) + C_PetBattles.GetStateValue(petOwner, 0, 41) + C_PetBattles.GetStateValue(0, 0, 41)
 	end
The stateID 41 is "STATE_Stat_Accuracy". STATE_Stat_Accuracy updates constantly throughout the battle and sums up all of the accuracy effects on specified petOwner/petIndex combination. The first function call gets the accuracy modifier for the current pet and owner. This sum includes all accuracy buffs/debuffs affecting the target. The second function call checks the accuracy modifier for the current team as a whole and will sum any buffs/debuffs that are on the field (and not on a specific pet). The third function call (which is ignored if the pet is an Elemental due to their passive ability) checks the Game's field, which is the weather.

Note that STATE_Stat_Accuracy does not account for level differences between the active pets or abilities with conditional requirements to change their accuracy

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetAllStates}} - stateIDs are the table values of this function
* {{api|C_PetBattles.GetAbilityStateModification}} - another function that uses the stateID
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```