# API C GossipInfo.SelectActiveQuest

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Selects an active quest from the gossip window.
 C_GossipInfo.SelectActiveQuest(optionID)

==Arguments==
:;optionID:{{apitype|number}} - <code>questID</code> from {{api|C_GossipInfo.GetActiveQuests}}

==Patch changes==
* {{Patch 10.0.0|note=Changed <code>index</code> param to <code>optionID</code>.}}
* {{Patch 9.0.1|note=Moved to <code>C_GossipInfo.SelectActiveQuest()</code>}}
* {{Patch 1.0.0|note=Added as {{api|SelectGossipActiveQuest}}()}}
```