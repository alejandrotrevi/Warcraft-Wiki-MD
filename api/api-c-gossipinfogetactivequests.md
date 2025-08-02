# API C GossipInfo.GetActiveQuests

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Returns the quests which can be turned in at a quest giver.
 info = C_GossipInfo.GetActiveQuests()

==Returns==
:;info:{{apitype|GossipQuestUIInfo[]}}
{{:Struct GossipQuestUIInfo|nocaption=1}}

==Patch changes==
* {{Patch 9.0.1|note=Changed to <code>C_GossipInfo.GetActiveQuests()</code> and returns structured data.}}
* {{Patch 1.0.0|note=Added as {{api|GetGossipActiveQuests}}()}}

==See also==
* {{api|GetNumActiveQuests}}
* {{api|GetNumAvailableQuests}}
* {{api|C_GossipInfo.GetAvailableQuests}}
```