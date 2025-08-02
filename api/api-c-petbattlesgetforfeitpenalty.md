# API C PetBattles.GetForfeitPenalty

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the percentage of current health your pets will lose if you forfeit the battle.
 forfeitPenalty = C_PetBattles.GetForfeitPenalty()

==Returns==
:;forfeitPenalty:{{apitype|number}} - percentage of ''current'' health each pet in your team will lose, e.g. 10 meaning 10% of current health.

==Details==
* As the health loss is computed based on current health, it will never kill your pets.

==Patch changes==
* {{Patch 5.2.0|note=Added.}}

==See also==
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```