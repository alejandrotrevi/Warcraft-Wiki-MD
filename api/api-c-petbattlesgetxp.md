# API C PetBattles.GetXP

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the experience values of a specific pet in the current pet battle.
 xp, maxXp = C_PetBattles.GetXP(petOwner, petIndex)

==Arguments==
:;petOwner:{{apitype|number}} - 1: Current player, 2: Opponent
:;petIndex:{{apitype|number}} - Accepted values are 1-3, but the order is based on the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.

==Returns==
:;xp:{{apitype|number}} - Current experience progress towards the next level of the pet
:;maxXp:{{apitype|number}} - Total amount of experience required for the pet's current level to increase

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```