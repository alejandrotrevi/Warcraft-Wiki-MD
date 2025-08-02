# API C PetBattles.GetAbilityState

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a pet's ability's current state in the pet battle.
 isUsable, currentCooldown, currentLockdown = C_PetBattles.GetAbilityState(petOwner, petIndex, actionIndex)

==Arguments==
:;petOwner:{{apitype|number}} - 1: Current player, 2: Opponent
:;petIndex:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.
:;actionIndex:{{apitype|number}} - Accepted values are 1-3, corresponding to the ability buttons from left to right.

==Returns==
:;isUsable:{{apitype|boolean}} - if ability can be used
:;currentCooldown:{{apitype|number}} - turns until ability can be used (if not usable due to cooldown)
:;currentLockdown:{{apitype|number}} - turns until ability can be used (if not usable due to lockdowns, such as [[Nevermore (pet battle ability)|Nevermore]])

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.UseAbility}} - Use an ability
* {{api|C_PetBattles.IsSkipAvailable}} - Determine if skip is available to be used
* {{api|C_PetBattles.IsTrapAvailable}} - Determine if trap is available to be used
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```