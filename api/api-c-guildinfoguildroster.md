# API C GuildInfo.GuildRoster

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Requests updated guild roster information from the server.
 C_GuildInfo.GuildRoster()

==Details==
* {{api|t=e|GUILD_ROSTER_UPDATE}} fires when updated (but not necessarily altered) information is received from the server.
* The call will be ignored completely if the last GuildRoster() call was less than 10 seconds ago (most likely to limit the traffic caused by frequent opening/closing of the guild tab).

==Patch changes==
* {{Patch 8.2.0|note=Moved to <code>C_GuildInfo.GuildRoster()</code>}}
* {{Patch 1.0.0|note=Added as {{api|GuildRoster}}()}}

==See also==
* {{api|GetGuildRosterInfo}}
```