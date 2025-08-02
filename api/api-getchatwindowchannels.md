# API GetChatWindowChannels

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns subscribed channels for a chat window.
 channelName1, channelId1, ... = GetChatWindowChannels(frameId)

==Arguments==
:;frameId:{{apitype|number}} - The frame number of the chat frame to be queried (starts at 1).

==Returns==
:;channelName1:{{apitype|string}} - The name to display for the first channel.
:;channelId1:{{apitype|number}} - The 'zone channel' number for the first channel. Has a value of 0 for non-zone channels, and a non-zero value for zone channels (such as Trade, General)
:;...:{{apitype|list}} - Additional <code>channelName, channelId</code> pairs for each channel belonging to the chat window.

==Example==
This function is best called within a table constructor:
 local DefaultChannels = { GetChatWindowChannels(DEFAULT_CHAT_FRAME:GetID()) }

<!-- luals
---@param frameId number
---@return string channelName1
---@return number channelId1
---@return any ...
function GetChatWindowChannels(frameId) end
-->
```