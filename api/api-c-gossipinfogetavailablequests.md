# API C GossipInfo.GetAvailableQuests

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Returns the available quests at a quest giver.
 info = C_GossipInfo.GetAvailableQuests()

==Returns==
:;info:{{apitype|GossipQuestUIInfo[]}}
{{:Struct GossipQuestUIInfo|nocaption=1}}

==Details==
* ''Available'' quests are quests that the player does not yet have in their quest log.
* This list is available after {{api|t=e|GOSSIP_SHOW}} has fired.

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_GossipInfo.GetAvailableQuests()</code>}}
* {{Patch 1.0.0|note=Added as {{api|GetGossipAvailableQuests}}()}}

==See also==
* {{api|GetNumActiveQuests}}
* {{api|GetNumAvailableQuests}}
* {{api|C_GossipInfo.GetActiveQuests}}
```