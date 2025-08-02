# API GetQuestLogItemLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns item link for selected quest reward/choice/required item from quest log.
 itemLink = GetQuestLogItemLink(type, index)

==Arguments==
:;type:{{apitype|string}} - "required", "reward" or "choice"
:;index:{{apitype|table}} - Integer - Quest reward item index (starts with 1).


==Returns==
:;[[itemLink]]:{{apitype|string}} - The link to the quest item specified
:or nil, if the type and/or index is invalid, there is no active quest at the moment or if the server did not transmit the item information until the timeout (which can happen, if the item is not in the local item cache yet)


==Details==
: The active quest is being set when browsing the quest log. The quest log must not be open for this function to work, but a quest must be active.

:The different types refer to the different item lists, a quest can contain.
:"reward" is the list of items which will be granted upon finishing the quest.
:"choice" is the list of items the player can choose from, once the quest is finished.
:"required" should be the list of items which have to be handed in for the quest to be finished (this has not been verified)
```