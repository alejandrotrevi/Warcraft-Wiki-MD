# API CompleteQuest

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Continues the quest dialog to the reward selection step.
 CompleteQuest()

==Details==
* Unlike the name would suggest, this does not finalize the completion of a quest. Instead it is called when you press the continue button, and is used to continue from the progress dialog to the completion dialog. See {{api|GetQuestReward}}() for actually completing a quest.
* If you're interested in hooking the function called when completing a quest, check out QuestRewardCompleteButton_OnClick (in FrameXML\QuestFrame.lua) instead.
```