# API C PetBattles.GetAbilityInfoByID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns very detailed information about a specific ability.
 id, name, icon, maxCooldown, unparsedDescription, numTurns, petType, noStrongWeakHints = C_PetBattles.GetAbilityInfoByID(id)

==Arguments==
:;id:{{apitype|number}} - ID of the ability.

==Returns==
:;id:{{apitype|number}} - The ID of the ability returned back.
:;name:{{apitype|string}} - The name of the ability.
:;icon:{{apitype|string}} - The full path to the ability's icon.
:;maxCooldown:{{apitype|number}} - The normal cooldown period for the ability.
:;unparsedDescription:{{apitype|string}} - The ability's description in its pure and unparsed form.
:;numTurns:{{apitype|number}} - Duration of the ability. This is typically 1, but some abilities last multiple rounds.
:;petType:{{apitype|number}} - Returned values are 1-10, based on the {{Expand/API|battlePetTypeID|inline=}}
:;noStrongWeakHints:{{apitype|boolean}} - True if the ability should not show Strong/Weak indicators, false otherwise.

==Details==
*Despite falling under the realm of C_PetBattles, this function is incredibly useful outside Pet Battles too because it provides '''far''' more information than its C_PetJournal counterpart - {{api|C_PetJournal.GetPetAbilityInfo}}.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetJournal.GetPetAbilityInfo}} - Get information about a pet ability when you don't know the abilityID
* {{api|C_PetJournal.GetPetAbilityList}} - Get list of abilities for the specified pet species
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```