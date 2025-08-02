# API GetGossipActiveQuests

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of active quests from a gossip NPC. For getting the number of active quests from a non-gossip NPC see {{api|GetNumActiveQuests}}.
 title1, level1, isLowLevel1, isComplete1, isLegendary1, isIgnored1, title2, ... = GetGossipActiveQuests()

==Returns==
The following six return values are provided for each active quest:
:;title:{{apitype|string}} - The name of the quest
:;level:{{apitype|number}} - The level of the quest
:;isLowLevel:{{apitype|boolean}} - true if the quest is low level, false otherwise
:;isComplete:{{apitype|boolean}} - true if the quest is complete, false otherwise
:;isLegendary:{{apitype|boolean}} -  true if the quests is a legendary quest, false otherwise
:;isIgnored:{{apitype|boolean}} - true if the quests has been ignored, false otherwise

==Details==
The active quests for an NPC are available after {{api|GOSSIP_SHOW|t=e}} has fired.

==Patch changes==
* {{Patch 8.2.5|note=Added <code>questID</code> return value, increasing the number of returns to seven per active quest.<ref>{{ref FrameXML|GossipFrame.lua|8.2.5|31960|165|20190924}}</ref>}}
* {{Patch 7.0.3|note=Added <code>isIgnored</code> return value, increasing the number of returns to six per active quest.<ref>{{ref FrameXML|GossipFrame.lua|7.0.3|22267|129|20160719}}</ref>}}
* {{Patch 5.0.4|note=Added <code>isLegendary</code> return value, increasing the number of returns to five per active quest.<ref>{{ref FrameXML|GossipFrame.lua|5.0.4|16016|125|20120821}}</ref>}}

==See also==
* {{api|GetGossipAvailableQuests}}
* {{api|GetNumAvailableQuests}}
* {{api|GetNumActiveQuests}}

==References==
{{reflist|2}}
```