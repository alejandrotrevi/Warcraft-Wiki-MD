# API GetNumQuestLogRewards

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of unconditional rewards for the current quest in the quest log.
 numQuestRewards = GetNumQuestLogRewards([questID])

==Arguments==
:;questID:{{apitype|number?}}

==Returns==
:;numQuestRewards:{{apitype|number}} - The number of rewards for this quest

==Details==
* This refers to items always awarded upon quest completion; for quests where the player is allowed to choose a reward, see {{api|GetNumQuestLogChoices}}().
```