# API SelectGossipAvailableQuest

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Selects an available quest from a gossip list.
 SelectGossipAvailableQuest(index)

==Arguments==
:;index:{{apitype|number}} - Index of the available quest to select, from 1 to {{api|GetNumGossipAvailableQuests}}(); order corresponds to the order of return values from {{api|GetGossipAvailableQuests}}().

==Triggers events==
* {{api|t=e|QUEST_PROGRESS}} is fired when the details of the quest are available.
```