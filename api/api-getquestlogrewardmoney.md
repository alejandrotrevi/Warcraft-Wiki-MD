# API GetQuestLogRewardMoney

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|Quest}}
Returns the amount of money rewarded for a quest.
 money = GetQuestLogRewardMoney([questID])

==Arguments==
:;questID:{{apitype|number?}} - Unique identifier for a quest.

==Returns==
:;money:{{apitype|number}} - The amount of copper this quest gives as a reward

==Details==
* The questID argument is optional. When called without an questID, returns for the most recently viewed quest in the quest log window.
* Returns 0 if the questID is not currently in the quest log.
```