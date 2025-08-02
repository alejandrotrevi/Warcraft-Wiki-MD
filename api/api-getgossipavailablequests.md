# API GetGossipAvailableQuests

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of available quests from a gossip NPC. For getting the number of available quests from a non-gossip NPC see {{api|GetNumAvailableQuests}}.
 title1, level1, isTrivial1, frequency1, isRepeatable1, isLegendary1, isIgnored1, title2, ... = GetGossipAvailableQuests()

==Returns==
The following seven return values are provided for each quest offered by the NPC:
:;title:{{apitype|string}} - The name of the quest.
:;level:{{apitype|number}} - The level of the quest.
:;isTrivial:{{apitype|boolean}} - true if the quest is trivial (too low-level compared to the character), false otherwise.
:;frequency:{{apitype|number}} - 1 if the quest is a normal quest, <code>LE_QUEST_FREQUENCY_DAILY</code> (2) for daily quests, <code>LE_QUEST_FREQUENCY_WEEKLY</code> (3) for weekly quests.
:;isRepeatable:{{apitype|boolean}} - true if the quest is repeatable, false otherwise.
:;isLegendary:{{apitype|boolean}} - true if the quest is a legendary quest, false otherwise.
:;isIgnored:{{apitype|boolean}} - true if the quest has been ignored, false otherwise.

==Details==
* ''Available'' quests are quests that the player does not yet have in their quest log.
* This list is available after {{api|t=e|GOSSIP_SHOW}} has fired.

==Patch changes==
* {{Patch 8.2.5|note=Added <code>questID</code> return value.<ref>{{ref FrameXML|GossipFrame.lua|8.2.5|31960|20, 138, and 144|20190924}}</ref>}}
* {{Patch 7.0.3|note=Added <code>isIgnored</code> return value.<ref>{{ref FrameXML|GossipFrame.lua|7.0.3|22267|83|20160719}}</ref>}}
* {{Patch 6.0.2|note=Changed boolean returns from 1/nil to true/false.{{fact}} Changed <code>isDaily</code> return value to <code>frequency</code>.<ref>{{ref FrameXML|GossipFrame.lua|6.0.2|19033|86|20141014}}</ref>}}
* {{Patch 5.0.4|note=Added <code>isLegendary</code> return value.<ref>{{ref FrameXML|GossipFrame.lua|5.0.4|16016|78|2012-08-21}}</ref>}}

==See also==
* {{api|GetGossipActiveQuests}}
* {{api|GetNumAvailableQuests}}
* {{api|GetNumActiveQuests}}

==References==
{{reflist|2}}
```