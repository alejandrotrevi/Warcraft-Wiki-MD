# API GetQuestLogRewardSpell

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|Quest}}
Returns the spell reward for a quest.
 texture, name, isTradeskillSpell, isSpellLearned, hideSpellLearnText, isBoostSpell, garrFollowerID, genericUnlock, spellID = GetQuestLogRewardSpell(rewardIndex, questID)

==Arguments==
:;rewardIndex:{{apitype|number}} - The index of the spell reward to get the details for, from 1 to {{api|GetNumRewardSpells}}
:;questID:{{apitype|number}} - Unique [[QuestID]] for the quest to be queried.

==Returns==

:;texture:{{apitype|string}} - The texture of the spell icon
:;name:{{apitype|string}} - The spell name
:;isTradeskillSpell:{{apitype|boolean}} - Whether the spell is a tradeskill spell
:;isSpellLearned:{{apitype|boolean}} - Whether the spell has been learned already
:;hideSpellLearnText:{{apitype|unknown}}
:;isBoostSpell:{{apitype|boolean}} - Unknown
:;garrFollowerID:{{apitype|number}} - If the spell grants a Garrison follower, it's ID.
:;genericUnlock:{{apitype|unknown}}
:;spellID:{{apitype|number}} - Unknown

==Description==
Returns information about the spell reward of the current selected quest.
```