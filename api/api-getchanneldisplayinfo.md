# API GetChannelDisplayInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for chat channels and headers in the Chat Pane.
 name, header, collapsed, channelNumber, count, active, category, channelType = GetChannelDisplayInfo(index)

==Arguments==
:;index:{{apitype|number}} - an integer between 1 and GetNumDisplayChannels() (ChannelFrame can display a combined maximum of 20 channels and headers; see MAX_CHANNEL_BUTTONS and use [[API GetNumDisplayChannels]])

==Returns==
:;name:{{apitype|string}} - (''for channels'') channel name; (''for headers'') name of the header
:;header:{{apitype|boolean}} - true if this item is a header (e.g. for category "CHANNEL_CATEGORY_WORLD")
:;collapsed:{{apitype|boolean?}} - (''for headers'') true if subchannels are hidden (header is collapsed), otherwise false or nil
:;channelNumber:{{apitype|number?}} - (''for channels'') channel number, nil otherwise
:;count:{{apitype|number?}} - (''for channels'') number of players in this channel; (''for headers'') number of subchannels beneath this header, nil otherwise
:;active:{{apitype|boolean?}} - (''for channels'') true if channel is active (if you leave a city where you were in Trade Channel the channel will remain as inactive), nil otherwise
:;category:{{apitype|string}} - (''for channels'') "CHANNEL_CATEGORY_WORLD", "CHANNEL_CATEGORY_GROUP" or "CHANNEL_CATEGORY_CUSTOM"
:;channelType:{{apitype|number}}

==See also==
* [[API_GetNumDisplayChannels|GetNumDisplayChannels()]]
* [[API_GetChannelList|GetChannelList()]]
* [[API_SendChatMessage|SendChatMessage()]]
```