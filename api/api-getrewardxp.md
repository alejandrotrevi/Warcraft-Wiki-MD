# API GetRewardXP

**Contributor:** Dark T Zeratul

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the [[experience]] reward for the quest in the gossip window.
 xp = GetRewardXP()

==Arguments==
None

==Returns==
:;xp:{{apitype|number}} - Amount of experience points to be received upon completing the quest, including any bonuses to experience gain such as [[Rest]] and [[Enlightenment (buff)]].

==Details==
* This function is not related to your quest log.
* The return values update when the {{api|t=e|QUEST_DETAIL}}, {{api|t=e|QUEST_COMPLETE}} events fire.
```