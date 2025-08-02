# API GetQuestResetTime

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of seconds until daily quests reset.
 nextReset = GetQuestResetTime()

==Returns==
:;nextReset:{{apitype|number}} - Number of seconds until the next daily quest reset.

==Details==
* At the first UI load per login, this function returns the time since the Unix epoch instead. Appears to give the correct value as of the ''second'' {{api|t=e|QUEST_LOG_UPDATE}} event to occur after login.
* In 6.x returned incorrect answers for players inside instances hosted on servers that use a different reset time (eg Oceanic and Brazilian players in US continental instance servers). Fixed in 7.x
A simple test case:
 print("init", GetQuestResetTime())
 
 local frame = CreateFrame("Frame")
 frame:RegisterEvent("PLAYER_LOGIN")
 frame:RegisterEvent("QUEST_LOG_UPDATE")
 frame:SetScript("OnEvent", function(self, event)
     print(event, GetQuestResetTime())
 end)
```