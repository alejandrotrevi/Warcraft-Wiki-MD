# API GetWorldElapsedTime

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
 description, elapsedTime, type = GetWorldElapsedTime(timerID)

==Arguments==
:;timerID:{{apitype|number}}

==Returns==
:;description:{{apitype|string}}
:;elapsedTime:{{apitype|number}}
:;type:{{apitype|number}}

==Details==
* 'type' returns one of
** LE_WORLD_ELAPSED_TIMER_TYPE_PROVING_GROUND
** LE_WORLD_ELAPSED_TIMER_TYPE_CHALLENGE_MODE
** LE_WORLD_ELAPSED_TIMER_TYPE_NONE

==Patch changes==
* {{Patch 5.4.0|note=type changed from bolean isChallangeMode to event listed in details}}
```