# API GetLFGQueueStats

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the current LFG queue.
 hasData, leaderNeeds, tankNeeds, healerNeeds, dpsNeeds, totalTanks, totalHealers, totalDPS, instanceType, instanceSubType, instanceName, averageWait, tankWait, healerWait, dpsWait, myWait, queuedTime, activeID = GetLFGQueueStats(category [, activeID])

==Arguments==
The first argument has two forms, affecting how the function behaves (see details):
:;category:{{apitype|number}} - Depending on which type of LFG you're looking for.
:;activeID:{{apitype|number?}} - Specific LFG 'forming group' ID

==Returns==
:;1. hasData:{{apitype|boolean}}  - indicates if you are in queue
:;2. leaderNeeds:{{apitype|boolean}} - if group still needs a leader designated
:;3. tankNeeds:{{apitype|boolean}} - waiting for a tank
:;4. healerNeeds:{{apitype|boolean}} - waiting for a designated healer
:;5. dpsNeeds:{{apitype|boolean}} - needing more DPS'ers
:;6. totalTanks:{{apitype|number}} - total tanks needed for this queue
:;7. totalHealers:{{apitype|number}} - total healers needed for this queue
:;8. totalDPS:{{apitype|number}} - total DPS'ers needed for this queue
:;9. instanceType:{{apitype|number}} - unknown relation
:;10. instanceSubType:{{apitype|number}} - unknown relation
:;11. instanceName:{{apitype|string}} - as selected in LFD Finder
:;12. averageWait:{{apitype|number}} - average wait for an entire group to be assembled
:;13. tankWait:{{apitype|number}} - average wait time for queuing Tanks
:;14. healerWait:{{apitype|number}} - average wait time for queuing Healers
:;15. dpsWait:{{apitype|number}} - average wait time for queuing DPS'ers
:;16. myWait:{{apitype|number}} - predicted wait time for you
:;17. queuedTime:{{apitype|number}} - appears to be the absolute time of when the queue began.  Use against [[API GetTime|GetTime]]()
:;18. activeID:{{apitype|number}}

==Patch changes==
* {{Patch 5.4.0|note=Added <code>activeID</code> argument/return.}}

==See also==
* {{api|t=e|LFG_QUEUE_STATUS_UPDATE}} - Indicates new data is available.
```