# API GetQuestLogTitle

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a quest in your quest log.
 title, level, suggestedGroup, isHeader, isCollapsed, isComplete, frequency, questID, startEvent, displayQuestID, isOnMap, hasLocalPOI, isTask, isBounty, isStory, isHidden, isScaling = GetQuestLogTitle(questLogIndex)

==Arguments==
:;questLogIndex:{{apitype|number}} - The index of the quest you wish to get information about, between 1 and [[API_GetNumQuestLogEntries|GetNumQuestLogEntries()]]'s first return value.

==Returns==
:;1. title:{{apitype|string}} - The title of the quest, or nil if the index is out of range. 
:;2. level:{{apitype|number}} - The level of the quest.
:;3. suggestedGroup:{{apitype|number}} - If the quest is designed for more than one player, it is the number of players suggested to complete the quest. Otherwise, it is 0.
:;4. isHeader:{{apitype|boolean}} - true if the entry is a header, false otherwise.
:;5. isCollapsed:{{apitype|boolean}} - true if the entry is a collapsed header, false otherwise.
:;6. isComplete:{{apitype|number}} - 1 if the quest is completed, -1 if the quest is failed, nil otherwise.
:;7. frequency:{{apitype|number}} - 1 if the quest is a normal quest, <code>LE_QUEST_FREQUENCY_DAILY</code> (2) for daily quests, <code>LE_QUEST_FREQUENCY_WEEKLY</code> (3) for weekly quests.
:;8. questID:{{apitype|number}} - The quest identification number. This is the number found in GetQuestsCompleted() after it has been completed. It is also the number used to identify quests on sites such as Wowhead.com (Example: [http://www.wowhead.com/?quest=2158 Rest and Relaxation])
:;9. startEvent:{{apitype|boolean}} - ?
:;10. displayQuestID:{{apitype|boolean}} - true if the <code>questID</code> is displayed before the title, false otherwise.
:;11. isOnMap:{{apitype|boolean}} - ?
:;12. hasLocalPOI:{{apitype|boolean}} - ?
:;13. isTask:{{apitype|boolean}} - ?
:;14. isBounty:{{apitype|boolean}} - ? (true for Legion World Quests; is it true for other WQs?)
:;15. isStory:{{apitype|boolean}} - ?
:;16. isHidden:{{apitype|boolean}} - true if the quest is not visible inside the player's quest log.
:;17. isScaling:{{apitype|boolean}} - ?

==Example==
  local i = 1
  while GetQuestLogTitle(i) do
   local title, level, suggestedGroup, isHeader, isCollapsed, isComplete, frequency, questID, startEvent, displayQuestID, isOnMap, hasLocalPOI, isTask, isBounty, isStory, isHidden, isScaling = GetQuestLogTitle(i)
   if ( not isHeader ) then
    DEFAULT_CHAT_FRAME:AddMessage(title .. " [" .. level .. "] " .. questID)
   end
   i = i + 1
  end

===Result===
Prints the name, level, and Quest ID of all quests in your quest log.

==Patch changes==
* {{Patch 7.0.3|note=Added the 'isBounty' return.}}
* {{Patch 6.0.2|note=Removed returns 'questTag' and 'isDaily'. Added returns 'frequency', 'isOnMap', 'hasLocalPOI', 'isTask', and 'isStory'.}}
* {{Patch 3.3.0|note=Added the 'questID' return.}}
* {{Patch 2.1.0|note=Added the 'isDaily' return.}}
* {{Patch 2.0.3|note=Added the 'suggestedGroup' return.}}
```