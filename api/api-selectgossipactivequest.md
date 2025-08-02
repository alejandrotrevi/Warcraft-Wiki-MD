# API SelectGossipActiveQuest

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Selects an active quest from a gossip list.  
 SelectGossipActiveQuest(index)

==Arguments==
:;index:{{apitype|number}} - Index of the active quest to select, from 1 to {{api|GetNumGossipActiveQuests}}(); order corresponds to the order of return values from {{api|GetGossipActiveQuests}}().

==Triggers events==
* {{api|t=e|QUEST_PROGRESS}} is fired when the details of the quest are available.
```