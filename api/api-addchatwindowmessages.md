# API AddChatWindowMessages

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Enables messages from the chat message type (e.g. "SAY") for a chat window.
 AddChatWindowMessages(index, messageGroup)

==Arguments==
:;index:{{apitype|number}} - The chat window index, ascending from 1.
:;messageGroup:{{apitype|string}} - Message group to add to the chat window, e.g. "SAY", "EMOTE", "MONSTER_BOSS_EMOTE".

==See also==
* {{api|GetChatWindowMessages}}
* {{api|RemoveChatWindowMessages}}
* {{api|AddChatWindowChannel}}
```