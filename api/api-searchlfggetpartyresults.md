# API SearchLFGGetPartyResults

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the party player listed in raid browser.
 local name, level, relationship, className, areaName, comment, isLeader, isTank, isHealer, isDamage, bossKills, specID, isGroupLeader, armor, spellDamage, plusHealing, CritMelee, CritRanged, critSpell, mp5, mp5Combat, attackPower, agility, maxHealth, maxMana, gearRating, avgILevel, defenseRating, dodgeRating, BlockRating, ParryRating, HasteRating, expertise = SearchLFGGetPartyResults(index, partyIndex)

==Arguments==
:;index:{{apitype|number}} - Index of the player to query, ascending from 1 to totalResults return value from {{api|SearchLFGGetNumResults}}.
:;partyIndex:{{apitype|number}} - Index of the party player to query, ascending from 1 to partyMembers return value from {{api|SearchLFGGetResults}}.

==Returns==
:;name:{{apitype|string}} - Name of the player.
:;level:{{apitype|number}} - Player level.
:;areaName:{{apitype|string}} - Player's area.
:;comment:{{apitype|string}} - Player's custom comment.
:;bossKills:{{apitype|number}} - Sum of all boss kills on normal mode
:;gearRating:{{apitype|number}} - Some weird value only blizzard has clue about

==See also==
* {{api|SearchLFGGetResults}}()

<!-- luals
---@param index number
---@param partyIndex number
---@return any ...
function SearchLFGGetPartyResults(index, partyIndex) end
-->
```