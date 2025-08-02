# API GetRewardSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the spell reward for the quest in the gossip window.
 texture, name, isTradeskillSpell, isSpellLearned = GetRewardSpell()

==Returns==
texture, name, isTradeskillSpell, isSpellLearned 

:texture - icon of spell.
:name - name of spell.
:isTradeskillSpell - if spell received is a tradeskill or not. This will be true, for example, for quests that upgrade your secondary professions, like fishing quest from Nat Pagle.
:isSpellLearned - if you actually learn a spell and it will appear in your spellbook (true) or if it will be just cast on you (false).

==Details==
Just as almost any other quest gossip function, GetRewardSpell() returns data that refreshes only when you see corresponding gossip page. Any subsequent calls will return same data until next update. You can watch updates for data returned by GetRewardSpell() by registering for QUEST_DETAIL and QUEST_COMPLETE events. This means that if, for example, you talk to some NPC and check details of quest that offers spell reward and then talk to another NPC and check progress gossip page of quest you've accepted previously that offers spell reward too, this function will still return data of spell from first quest because progress page does not show rewards and their data is not updated.
```