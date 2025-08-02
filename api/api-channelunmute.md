# API ChannelUnmute

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Unmutes the specified user on the channel.
 ChannelUnmute(channelName, playerName)

==Arguments==
:;channelName:{{apitype|string}} - The name of the channel to remove mute on
:;playerName:{{apitype|string}} - The name of the player to remove mute from (allow to speak)

==See also==
* {{api|ChannelMute}}

==Example==
 ChannelUnmute("uimods", "Sembiance");
```