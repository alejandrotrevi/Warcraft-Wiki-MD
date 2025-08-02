# API QuestPOIGetIconInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns WorldMap POI icon information for the given quest.
 completed, posX, posY, objective = QuestPOIGetIconInfo(questId)

==Arguments==
:;questId:{{apitype|number}} - you can get this from the [[QuestLink|quest link]] or from [[API_GetQuestLogTitle|GetQuestLogTitle]](questLogIndex).

==Returns==
:;completed:{{apitype|boolean}} - is the quest completed (the icon is a question mark).
:;posX:{{apitype|number}} (between 0 and 1 inclusive) - the X position where the icon is shown on the map.
:;posY:{{apitype|number}} (between 0 and 1 inclusive) - the Y position where the icon is shown on the map.
:;objective:{{apitype|number}} - which is sometimes negative and doesn't appear to have anything to do with the quest's actual objectives.

==Example==
 local playerX, playerY = GetPlayerMapPosition("player")
 local _, questX, questY = QuestPOIGetIconInfo(12345)
 local diffX, diffY = abs(playerX - questX), abs(playerY - questY)
 local distanceToTarget = math.sqrt(math.pow(diffX, 2) + math.pow(diffY, 2))
 print("You are ", floor(distanceToTarget * 100), " clicks from the target location.")

==Results==
 You are 42 clicks from the target location.
```