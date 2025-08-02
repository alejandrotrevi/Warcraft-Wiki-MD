# API C PetBattles.GetAttackModifier

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the modifier for an attack launched by a pet against an enemy pet.
 modifier = C_PetBattles.GetAttackModifier(petType, enemyPetType)

==Arguments==
:;petType:{{apitype|number}} - Index of the pet's type. Accepted values are 1-10.
:;enemyPetType:{{apitype|number}} - Index of the enemy pet's type. Accepted values are 1-10.

==Returns==
:;modifier:{{apitype|number}} - The multiplier that should be applied to an attack from petType launched against enemyPetType.

==Returns==
The returns are currently either: 1 (default), 0.666667 (weak), or 1.5 (strong)

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```