# API GetBattlefieldScore

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a player's score in battlefields.
 name, killingBlows, honorableKills, deaths, honorGained, faction, race, class, classToken, damageDone, healingDone, bgRating, ratingChange, preMatchMMR, mmrChange, talentSpec = GetBattlefieldScore(index)

==Arguments==
:;index:{{apitype|number}} - The characters index in battlegrounds, going from 1 to [[API GetNumBattlefieldScores|GetNumBattlefieldScores]]().

==Returns==
:;name:{{apitype|string}} - The player's name, with their server name attached if from a different server to the player.
:;killingBlows:{{apitype|number}} - Number of killing blows.
:;honorableKills:{{apitype|number}} - Number of honorable kills.
:;deaths:{{apitype|number}} - The number of deaths.
:;honorGained:{{apitype|number}} - The amount of honour gained so far (Bonus Honour).
:;faction:{{apitype|number}} - (Battlegrounds: Horde = 0, Alliance = 1 / Arenas: Green Team = 0, Yellow Team = 1).
:;race:{{apitype|string}} - The players race (Orc, Undead, Human, etc).
:;class:{{apitype|string}} - The players class (Mage, Hunter, Warrior, etc).
:;classToken:{{apitype|string}} - The player's class name in english given in all capitals (MAGE , HUNTER, WARRIOR, etc)
:;damageDone:{{apitype|number}} - The amount of damage done.
:;healingDone:{{apitype|number}} - The amount of healing done.
:;bgRating:{{apitype|number}} - Personal battleground rating at the start of the match
:;ratingChange:{{apitype|number}} - Amount of rating gained/lost during the match
:;preMatchMMR:{{apitype|number}} - After 4.2 update is always zero
:;mmrChange:{{apitype|number}} - After 4.2 update is always zero
:;talentSpec:{{apitype|string}} - Localized name of player build

==Example==
How to count the number of players in each faction.

 local numScores = GetNumBattlefieldScores()
 local numHorde = 0
 local numAlliance = 0
 for i=1, numScores do
 	name, killingBlows, honorableKills, deaths, honorGained, faction = GetBattlefieldScore(i);
 	if ( faction ) then
 		if ( faction == 0 ) then
 			numHorde = numHorde + 1
 		else
 			numAlliance = numAlliance + 1
 		end
 	end
 end
```