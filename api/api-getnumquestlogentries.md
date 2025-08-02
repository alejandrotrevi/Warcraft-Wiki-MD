# API GetNumQuestLogEntries

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of entries in the quest log.
 numEntries, numQuests = GetNumQuestLogEntries()

==Returns==
:;numEntries:{{apitype|number}} - Number of entries in the Quest Log, including collapsable zone headers.
:;numQuests:{{apitype|number}} - Number of actual quests in the Quest Log, not counting zone headers.

==Example==
This snippet displays the number of visible entries (headers and non-collapsed quests) in the quest log and quest count total to the default chat frame.
 local numEntries, numQuests = GetNumQuestLogEntries()
 print(numEntries .. " entries containing " .. numQuests .. " quests in your quest log.");
```