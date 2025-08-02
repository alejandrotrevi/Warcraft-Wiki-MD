# API RemoveChatWindowMessages

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Removes the specified chat message type from a chat window.
 RemoveChatWindowMessages(index, messageGroup)

==Arguments==
:;index:{{apitype|number}} - chat window index, ascending from 1.
:;messageGroup:{{apitype|string}} - message type the chat window should no longer receive, e.g. "EMOTE", "SAY", "RAID".

==See also==
* {{api|AddChatWindowMessages}}
* {{api|GetChatWindowMessages}}
```