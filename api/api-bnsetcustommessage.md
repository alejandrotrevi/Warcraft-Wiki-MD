# API BNSetCustomMessage

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Sends a broadcast message to your Real ID friends.
 BNSetCustomMessage(text)

==Arguments==
:;text:{{apitype|string}} - message to be broadcasted (max 127 chars)

==Details==
* Triggers {{api|t=e|CHAT_MSG_BN_INLINE_TOAST_BROADCAST}} (receiver)
* Triggers {{api|t=e|CHAT_MSG_BN_INLINE_TOAST_BROADCAST_INFORM}} (sender) <font color="#F6ADC6">"Your broadcast has been sent."</font>
* See {{api|BNGetInfo}}() for the current broadcast message.

==Example==
Sets your broadcast message.
<syntaxhighlight lang="lua">
BNSetCustomMessage("Hello friends!")
</syntaxhighlight>

Clears your broadcast message.
 BNSetCustomMessage("")
```