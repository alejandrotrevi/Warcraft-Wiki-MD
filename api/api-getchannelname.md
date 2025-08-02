# API GetChannelName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a chat channel.
 id, name, instanceID, isCommunitiesChannel = GetChannelName(name)

==Arguments==
:;name:{{apitype|string,number}} - name of the channel to query, e.g. "Trade - City", or a channel ID to query, e.g. 1 for the chat channel currently addressable using /1.

==Returns==
:;id:{{apitype|number}} - The ID of the channel, or 0 if the channel is not found.
:;name:{{apitype|string}} - The name of the channel, e.g. "Trade - Stormwind", or nil if the player is not in the queried channel.
:;instanceID:{{apitype|number}} - Index used to deduplicate channels. Usually zero, unless two channels with the same name exist.
:;isCommunitiesChannel:{{apitype|boolean}} - True if this is a Blizzard Communities channel, false if not.

==Details==
* Note that querying GetChannelName("Trade - City") may return values which appear to be valid even while the player is not a city. Consider using <code>GetChannelName((GetChannelName("Trade - City"))) > 0</code> to check whether you really have access to the Trade channel.

==Patch changes==
* {{Patch 8.0.1|note=Added <code>isCommunitiesChannel</code> return.}}
```