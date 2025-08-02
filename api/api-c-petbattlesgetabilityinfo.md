# API C PetBattles.GetAbilityInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns ability information for an ability in a slot on a pet that you own.
 id, name, icon, maxCooldown, unparsedDescription, numTurns, petType, noStrongWeakHints = C_PetBattles.GetAbilityInfo(petOwner, petIndex, abilityIndex)

==Arguments==
:;petOwner:{{apitype|number}} - 1: Current player, 2: Opponent
:;petIndex:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.
:;abilityIndex:{{apitype|number}} - Accepted values are 1-3, corresponding to the ability in the slot with that number.

==Returns==
:;id:{{apitype|number}} - The ID of the ability returned back.
:;name:{{apitype|string}} - The name of the ability.
:;icon:{{apitype|string}} - The full path to the ability's icon.
:;maxCooldown:{{apitype|number}} - The normal cooldown period for the ability.
:;unparsedDescription:{{apitype|string}} - The ability's description in its pure and unparsed form.
:;numTurns:{{apitype|number}} - Duration of the ability. This is typically 1, but some abilities last multiple rounds.
:;petType:{{apitype|number}} - Returned values are 1-10, based on the pet's type.
:;noStrongWeakHints:{{apitype|boolean}} - True if the ability should not show Strong/Weak indicators, false otherwise.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetAbilityInfoByID}} - an alternative way to get the same information
* {{api|C_PetJournal.GetPetAbilityList}} - the slot numbers are the indexes in the idTable from this function
* {{api|C_PetBattles.GetAbilityEffectInfo}} - return ability specific effects
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```