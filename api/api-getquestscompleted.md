# API GetQuestsCompleted

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of quests the character has completed in its lifetime.
 questsCompleted = GetQuestsCompleted([table])

==Arguments==
:;table:{{apitype|table}} - If supplied, fills this table with quests. Any other keys will be unchanged.

==Returns==
:;questsCompleted:{{apitype|table}} - The list of completed quests, keyed by quest IDs.

==Details==
* A quest appears in the list only after it has been completed and turned in, not while it is in your log.
* Completing certain quests can cause other quests (alternate versions, etc.) to appear completed also.
* Some quests are invisible.  These quests are not offered to players but suddenly become "completed" due to some other in-game occurrence.
* [[Daily quest]]s appear completed only if they have been completed that day.
* [[Pet_Battle_System|Pet Battle]] quests are account-wide and will be returned from this API across all characters. They can be discerned with {{api|GetQuestTagInfo}}() tagID 102.

==Example==
Prints completed questIds and their names (quest data gets cached from the server after the first query)
 for id in pairs(GetQuestsCompleted()) do
 	local name = C_QuestLog.GetQuestInfo(id)
 	print(id, name)
 end

For a fresh Human Priest who only completed two starter quests: [[Beating Them Back!]] ([https://www.wowhead.com/quest=28763/beating-them-back 28763]) and [[Lions for Lambs]] ([https://www.wowhead.com/quest=28771/lions-for-lambs 28771])
 /dump GetQuestsCompleted()

 {
 	[28757] = true, -- "Beating Them Back!" -- Mage
 	[28762] = true, -- "Beating Them Back!" -- Paladin
 	[28763] = true, -- "Beating Them Back!" -- Priest
 	[28764] = true, -- "Beating Them Back!" -- Rogue
 	[28765] = true, -- "Beating Them Back!" -- Warlock
 	[28766] = true, -- "Beating Them Back!" -- Warrior
 	[28767] = true, -- "Beating Them Back!" -- Hunter
 	[29078] = true, -- "Beating Them Back!" -- unknown
 	[31139] = true, -- "Beating Them Back!" -- Monk
 	[28759] = true, -- "Lions for Lambs"
 	[28769] = true, -- "Lions for Lambs"
 	[28770] = true, -- "Lions for Lambs"
 	[28771] = true, -- "Lions for Lambs" -- Priest
 	[28772] = true, -- "Lions for Lambs"
 	[28773] = true, -- "Lions for Lambs"
 	[28774] = true, -- "Lions for Lambs"
 	[29079] = true, -- "Lions for Lambs"
 	[31140] = true, -- "Lions for Lambs"
 }

==Patch changes==
* {{Patch 9.0.1|note=Changed to <code>C_QuestLog.GetAllCompletedQuestIDs()</code> and returns quest IDs in a sequentially ordered table instead of associative.}}
* {{Patch 5.0.4|note=No longer requires {{api|QueryQuestsCompleted}}() to be called before.}}
* {{Patch 3.3.0|note=Added as <code>GetQuestsCompleted()</code>}}

==See also==
* {{api|IsQuestFlaggedCompleted}}()
* {{api|C_QuestLog.GetQuestInfo}}()
```