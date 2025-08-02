# API CanAbandonQuest

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the player can abandon a specific quest
 canAbandon = CanAbandonQuest(questID)

==Arguments==
:;questID:{{apitype|number}} - quest ID of the quest to query, e.g. 5944 for [[In Dreams]]

==Returns==
:;canAbandon:{{apitype|boolean}} - 1 if the player is currently on the specified quest and can abandon it, nil otherwise.

==Details==
* Some quests cannot be abandoned. These include some of the Battle Pet Tamers quests.
```