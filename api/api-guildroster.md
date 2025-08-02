# API GuildRoster

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Requests updated guild roster information from the server.
 GuildRoster()

==Triggers events==
* {{api|t=e|GUILD_ROSTER_UPDATE}} fires when updated (but not necessarily altered) information is received from the server.

==Details==
* The call will be ignored completely if the last GuildRoster() call was less than 10 seconds ago (most likely to limit the traffic caused by frequent opening/closing of the guild tab).

==See also==
* {{api|GetGuildRosterInfo}}
```