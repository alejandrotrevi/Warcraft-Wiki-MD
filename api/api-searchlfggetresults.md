# API SearchLFGGetResults

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the player listed in raid browser.
 name, level, areaName, className, comment, partyMembers, status, class, encountersTotal, encountersComplete, isIneligible, isLeader, isTank, isHealer, isDamage, bossKills, specID, isGroupLeader, armor, spellDamage, plusHealing, CritMelee, CritRanged, critSpell, mp5, mp5Combat, attackPower, agility, maxHealth, maxMana, gearRating, avgILevel, defenseRating, dodgeRating, BlockRating, ParryRating, HasteRating, expertise = SearchLFGGetResults(index)

==Arguments==
:;index:{{apitype|number}} - Index of the player to query, ascending from 1 to totalResults return value from {{api|SearchLFGGetNumResults}}.

==Returns==
:;name:{{apitype|string}} - Name of the player.
:;level:{{apitype|number}} - Player level.
:;areaName:{{apitype|string}} - Player's area.
:;className:{{apitype|string}} - Player's class.
:;comment:{{apitype|string}} - Player's custom comment.
:;partyMembers:{{apitype|number}} - Count of players in the group.
:;bossKills:{{apitype|number}} - Sum of all boss kills on normal mode
:;gearRating:{{apitype|number}} - Some weird value only blizzard has clue about

==See also==
* {{api|SearchLFGGetPartyResults}}()

<!-- luals
---@param index number
---@return any ...
function SearchLFGGetResults(index) end
-->
```