# API GetFactionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a faction.
 name, description, standingID, barMin, barMax, barValue, atWarWith, canToggleAtWar, isHeader, isCollapsed, hasRep, isWatched, isChild, factionID, hasBonusRepGain, canBeLFGBonus 
     = GetFactionInfo(factionIndex)
     = GetFactionInfoByID(factionID)

==Arguments==
===<font color="#4ec9b0">GetFactionInfo</font>===
:;factionIndex:{{apitype|number}} - Index from the currently displayed row in the player's reputation pane, including headers but excluding factions that are hidden because their parent header is collapsed.
===<font color="#4ec9b0">GetFactionInfoByID</font>===
:;factionID:{{apitype|number}} : [[FactionID]]

==Returns==
:;1. name:{{apitype|string}} - Name of the faction
:;2. description:{{apitype|string}} - Description as shown in the detail pane that appears when you click on the faction row
:;3. standingID:{{apitype|number}} - [[API TYPE StandingId|StandingId]] representing the current standing (eg. 4 for Neutral, 5 for Friendly).
:;4. barMin:{{apitype|number}} - Minimum reputation since beginning of Neutral to reach the current standing.
:;5. barMax:{{apitype|number}} - Maximum reputation since the beginning of Neutral before graduating to the next standing.
:;6. barValue:{{apitype|number}} - Total reputation earned with the faction versus 0 at the beginning of Neutral.
:;7. atWarWith:{{apitype|boolean}} - True if the player is at war with the faction
:;8. canToggleAtWar:{{apitype|boolean}} - True if the player can toggle the "[[At War]]" checkbox
:;9. isHeader:{{apitype|boolean}} - True if the faction is a header (collapsible group title)
:;10. isCollapsed:{{apitype|boolean}} - True if the faction is a header '''and''' is currently collapsed
:;11. hasRep:{{apitype|boolean}} - True if the faction is a header '''and''' has its own reputation (eg. The Tillers)
:;12. isWatched:{{apitype|boolean}} - True if the "Show as Experience Bar" checkbox for the faction is currently checked
:;13. isChild:{{apitype|boolean}} - True if the faction is a second-level header (eg. Sholazar Basin) '''or''' is the child of a second-level header (eg. The Oracles)
:;14. factionID:{{apitype|number}} - Unique [[FactionID]].
:;15. hasBonusRepGain:{{apitype|boolean}} - True if the player has purchased a [[Grand Commendation]] to unlock bonus reputation gains with this faction
:;16. canSetInactive:{{apitype|boolean}}

==Details==
===Headers===
Top-level headers (eg. Cataclysm or Classic) return values for standingID, barMin, and barMax as if the player were at 0/3000 Neutral with a faction (4, 0, and 3000 respectively) except for the Inactive header, which returns values of 0.

Other headers that do not have their own reputation (eg. Sholazar Basin or Steamwheedle Cartel) return values for their child faction with which the player has the highest reputation. For example, if the player is 999/1000 Exalted with Booty Bay, 2900/21000 Revered with Everlook, 5300/12000 Honored with Gadgetzan, and 10/6000 Friendly with Ratchet, querying the Steamwheedle Cartel header will return the standingId, barMin, and barMax values for Booty Bay.

===Total Reputation===
Within the game reputation is shown as a formatted value of XXXX/YYYYY (eg. 1234/12000) but outside of the reputation tab these values are not avaliable directly. The game uses a flat value for reputation.

The earnedValue returned by GetFactionInfo( ) is NOT the value on your reputation bars, but instead the '''distance your reputation has moved from 0''' (1/3000 Neutral). All reputations given by the game are simply the number of reputation points from the 0 point, Neutral and above are positive reputations, anything below Neutral is a negative value and must be treated as such for any reputation calculations.

{|class="darktable" 
|-
! Game Value
! Standing
! Earned Value
! Breakdown
|-
| align="center"| 1/3000
| {{reputation|Neutral}}
| align="center"|1
| 1
|-
| align="center"| 1600/6000
| {{reputation|Friendly}}
| align="center"|4600
| 3000 + 1600
|-
| align="center"| 11000/12000
| {{reputation|Honored}}
| align="center"| 20000
| 3000 + 6000 + 11000
|-
| align="center"| 1400/3000
| {{reputation|Unfriendly}}
| align="center"| -1600
| -1600
|-
| align="center"| 2500/3000
| {{reputation|Hostile}}
| align="center"| -3500
| -3000 + -500
|}

Notice that for negative reputation that the Earned value is how far below 0 your reputation is, not how far till Hated or Exalted.

==Example==
Prints the name and total reputation earned for every faction currently displayed in the player's reputation pane:
<syntaxhighlight lang="lua">
for factionIndex = 1, GetNumFactions() do
	local name, description, standingId, bottomValue, topValue, earnedValue, atWarWith, canToggleAtWar,
		isHeader, isCollapsed, hasRep, isWatched, isChild, factionID = GetFactionInfo(factionIndex)
	if hasRep or not isHeader then
		DEFAULT_CHAT_FRAME:AddMessage("Faction: " .. name .. " - " .. earnedValue)
	end
end
</syntaxhighlight>

Prints the name and total reputation for all factions.
<syntaxhighlight lang="lua">
local numFactions = GetNumFactions()
local factionIndex = 1
while (factionIndex <= numFactions) do
	local name, description, standingId, bottomValue, topValue, earnedValue, atWarWith, canToggleAtWar,
		isHeader, isCollapsed, hasRep, isWatched, isChild, factionID, hasBonusRepGain, canBeLFGBonus = GetFactionInfo(factionIndex)
	if isHeader and isCollapsed then
		ExpandFactionHeader(factionIndex)
		numFactions = GetNumFactions()
	end
	if hasRep or not isHeader then
		DEFAULT_CHAT_FRAME:AddMessage("Faction: " .. name .. " - " .. earnedValue)
	end
	factionIndex = factionIndex + 1
end
</syntaxhighlight>

==See also==
* {{api|GetFriendshipReputation}}()
* {{api|GetFriendshipReputationRanks}}()

==Patch changes==
* {{Patch 9.1.5|note=Changed <code>canBeLFGBonus</code> return value to <code>canSetInactive</code>.}}
* {{Patch 5.2.0|note=Added new return values: ''hasBonusRepGain'', ''canBeLFGBonus''}}
* {{Patch 5.0.4|note=Added new return value: ''factionID''}}
```