# API C PetBattles.IsPlayerNPC

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether or not a pet battle team is controlled by an NPC.
 isNPC = C_PetBattles.IsPlayerNPC(petOwner)

==Arguments==
:;petOwner:{{apitype|number}} - 1: Current player, 2: Opponent.

==Returns==
:;isNPC:{{apitype|boolean}} - false if the pet owner is a player, true otherwise.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.IsWildBattle}}
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```