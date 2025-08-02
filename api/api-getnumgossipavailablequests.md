# API GetNumGossipAvailableQuests

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of quests (that you are not already on) offered by this NPC.
 numNewQuests = GetNumGossipAvailableQuests()

==Returns==
:;numNewQuests:{{apitype|number}} - Number of quests you can pick up from this NPC.

==Details==
* This information is available when {{api|t=e|GOSSIP_SHOW}} event fires.

==See also==
* {{api|GetGossipAvailableQuests}}
* {{api|SelectGossipAvailableQuest}}
```