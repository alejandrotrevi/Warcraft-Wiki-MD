# API AddChatWindowChannel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Enables messages from a chat channel index for a chat window.
 AddChatWindowChannel(windowId, channelName)

==Arguments==
:;windowId:{{apitype|number}} - index of the chat window/frame (ascending from 1) to add the channel to.
:;channelName:{{apitype|string}} - name of the chat channel to add to the frame.

==Details==
* A single channel may be configured to display in multiple chat windows/frames.
* Chat output architecture has changed since release; calling this function alone is no longer sufficient to add a channel to a particular frame in the default UI. Use {{api|ChatFrame_AddChannel}}(chatFrame, "channelName") instead, like so:
 ChatFrame_AddChannel(ChatWindow1, "Trade"); -- DEFAULT_CHAT_FRAME works well, too 

==See also==
* {{api|RemoveChatWindowChannel}}
```