# API C Reputation.GetFactionParagonInfo

**Contributor:** SirLeroy

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Reputation|system=ReputationInfo}}
Returns [[Paragon reputation|Paragon]] info on a faction.
 currentValue, threshold, rewardQuestID, hasRewardPending, tooLowLevelForParagon = C_Reputation.GetFactionParagonInfo(factionID)

==Arguments==
:;factionID:{{apitype|number}} : [[FactionID]]

==Returns==
:;currentValue:{{apitype|number}} - The amount of reputation you have earned in the current level of Paragon.
:;threshold:{{apitype|number}} - The amount of reputation until you gain the next Paragon level.
:;rewardQuestID:{{apitype|number}} - The ID of the quest once you attain a new Paragon level (or your first).
:;hasRewardPending:{{apitype|boolean}} - True if the player has attained a Paragon level but has not completed the reward quest.
:;tooLowLevelForParagon:{{apitype|boolean}} - True if the player level is too low to complete the Paragon reward quest.

==Details==
The <code>currentValue</code> return value contains a prefix that indicates the amount of paragon rewards you have gotten so far.
For example, having received a paragon reward for The Undying Army '''12''' times, if one calls the above function and the current rep level is '''717''', the result for ''currentValue ''will be '''120717'''.

==Example==
Reading the current reputation points of the venthyr covenant:
<syntaxhighlight lang="lua" line="1">
local factionID = 2413
local currentValue, threshold, rewardQuestID, hasRewardPending, tooLowLevelForParagon = C_Reputation.GetFactionParagonInfo(factionID)
-- total iterations (= Rewards Earned)
local level = ((math.floor(currentValue/threshold)*threshold)/10000) - (hasRewardPending and 1 or 0)
local realValue = currentValue % threshold

print("[",factionID, "]","current rep: ", realValue, " (", threshold, "), level: ", level)    
</syntaxhighlight>

==Patch changes==
* {{Patch 7.3.5|note=Added <code>tooLowLevelForParagon</code> return.}}
* {{Patch 7.2.0|note=Added.}}
```