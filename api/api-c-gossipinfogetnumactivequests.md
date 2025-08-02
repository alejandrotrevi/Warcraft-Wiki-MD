# API C GossipInfo.GetNumActiveQuests

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Returns the number of active quests that you should eventually turn in to this NPC.
 numQuests = C_GossipInfo.GetNumActiveQuests()

==Returns==
:;numQuests:{{apitype|number}}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_GossipInfo.GetNumActiveQuests()</code>}}
* {{Patch 2.3.0|note=Added as {{api|GetNumGossipActiveQuests}}()}}

==Details==
* This information is available when {{api|t=e|GOSSIP_SHOW}} event fires.
```