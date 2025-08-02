# API DeclineChannelInvite

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Declines an invitation to join a specific chat channel.
 DeclineChannelInvite(channel)

==Arguments==
:;channel:{{apitype|string}} - name of the channel the player was invited to but does not wish to join.

==Details==
* {{api|t=e|CHANNEL_INVITE_REQUEST}} fires when the player has been invited to a chat channel.
* There is no equivalent Accept function; FrameXML merely calls {{api|JoinPermanentChannel}} when the invitation is accepted.

==Patch changes==
* {{Patch 5.2.0|note=Added.}}
```