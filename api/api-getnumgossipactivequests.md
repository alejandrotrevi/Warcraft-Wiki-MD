# API GetNumGossipActiveQuests

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of active quests that you should eventually turn in to this NPC.
 numActiveQuests = GetNumGossipActiveQuests()

==Returns==
:;numActiveQuests:{{apitype|number}} - Number of quests you're on that should be turned in to the NPC you're gossiping with.

==Details==
* This information is available when {{api|t=e|GOSSIP_SHOW}} event fires.

==See also==
* {{api|GetGossipActiveQuests}}
* {{api|SelectGossipActiveQuest}}
```