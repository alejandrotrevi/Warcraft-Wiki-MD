# API C ChatBubbles.GetAllChatBubbles

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ChatBubbles|system=ChatBubbles}}
Returns all active chat bubbles.
 chatBubbles = C_ChatBubbles.GetAllChatBubbles([includeForbidden])

==Arguments==
:;includeForbidden:{{apitype|boolean?|default=false}}

==Returns==
:;chatBubbles:{{apitype|[[Widget_API#Frame|Frame]][]}}

==Details==
* Previously it was required to iterate over the WorldFrame children to access the chat bubbles.

==Patch changes==
* {{Patch 7.2.5|note=Added.}}
```