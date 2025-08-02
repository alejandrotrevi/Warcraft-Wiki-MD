# API GetQuestLogPushable

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the currently loaded quest in the quest window is able to be shared with other players.
 isPushable = GetQuestLogPushable()

==Returns==
:;isPushable:{{apitype|boolean}} - 1 if the quest can be shared, nil otherwise.

==Example==
  -- Determine whether the selected quest is pushable or not
  if ( GetQuestLogPushable() and GetNumPartyMembers() > 0 ) then
    QuestFramePushQuestButton:Enable();
  else
    QuestFramePushQuestButton:Disable();
  end
===Result===
QuestFramePushQuestButton is enabled or disabled based on whether the currently active quest is sharable (and you being in a party!).

==Details==
Use [[API_SelectQuestLogEntry|SelectQuestLogEntry(questID)]] to set the currently active quest before calling GetQuestLogPushable(). To initiate pushing (sharing) of a quest, use[[API QuestLogPushQuest|QuestLogPushQuest()]].
```