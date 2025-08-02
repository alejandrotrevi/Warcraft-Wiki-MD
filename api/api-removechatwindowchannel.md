# API RemoveChatWindowChannel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Removes the specified chat channel from a chat window.
 RemoveChatWindowChannel(windowId, channelName)

==Arguments==
:;windowId:{{apitype|number}} - index of the chat window/frame (ascending from 1) to remove the channel from.
:;channelName:{{apitype|string}} - name of the chat channel to remove from the frame.

==Details==
* Chat output architecture has changed since release; calling this function alone is no longer sufficient to block a channel from a particular frame in the default UI. Use {{api|ChatFrame_RemoveChannel}}(chatFrame, "channelName") instead, like so:
 ChatFrame_RemoveChannel(ChatWindow1, "Trade"); -- DEFAULT_CHAT_FRAME works well, too 

==See also==
* {{api|AddChatWindowChannel}}
```