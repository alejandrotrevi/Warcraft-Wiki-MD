# API JoinChannelByName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Joins the specified chat channel.
 type, name = JoinChannelByName(channelName [, password, frameID, hasVoice])

==Arguments==
:;channelName:{{apitype|string}} - The name of the channel to join. You can't use the "-" character in channelName.
:;password:{{apitype|string?}} - The channel password, nil if none.
:;frameID:{{apitype|number?}} - The chat frame ID number to add the channel to. Use [[API Frame GetID|Frame:GetID()]] to retrieve it for chat frame objects.
:;hasVoice:{{apitype|boolean}} - Enable voice chat for this channel.

==Returns==
:;type:{{apitype|number}} - The type of channel. 0 for a undefined channel, 1 for the zone General channel,  etc
:;name:{{apitype|string?}} - The name of the channel. 

==Example==
<syntaxhighlight lang="lua">
local channel_type, channel_name = JoinChannelByName("Mammoth", "thesane", ChatFrame1:GetID(), 1);
</syntaxhighlight>
```