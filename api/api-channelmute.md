# API ChannelMute

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Turns off the specified player's ability to speak in a channel.

 ChannelMute(channelName, playerName)

----
;''Arguments''

:(String channelName, String playerName)

:;channelName:The name of the channel to mute on
:;playerName:The name of the player to mute

----
;''Returns''

:;nil

----
;''Example''
 ChannelMute("uimods", "alexyoshi");

;''Result''

----
;''Description''

: Mutes player playerName on channel channelName, causing them to not be able to speak on that channel (spectator).
```