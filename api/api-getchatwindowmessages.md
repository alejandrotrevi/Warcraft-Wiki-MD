# API GetChatWindowMessages

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns subscribed message types for a chat window.
 type1, ... = GetChatWindowMessages(index)

==Arguments==
:;index:{{apitype|number}} - Chat window index, ascending from 1.

==Returns==
:;type1, ...:{{apitype|string}} - Chat type received by the window.

==See also==
* {{api|AddChatWindowMessages}}
* {{api|RemoveChatWindowMessages}}

<!-- luals
---@param index number
---@return string ...
function GetChatWindowMessages(index) end
-->
```