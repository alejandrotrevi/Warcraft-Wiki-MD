# API GetNumGuildMembers

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of total and online guild members.
 numTotal, numOnline = GetNumGuildMembers()

==Returns==
:;numTotal:{{apitype|number}} - Total number of players in the guild, or 0 if not in a guild.
:;numOnline:{{apitype|number}} - Number of players currently online, or 0 if not in a guild.

==Example==
Shows the total headcount of your guild and the number of online and offline people.
<syntaxhighlight lang="lua">
local numTotal, numOnline = GetNumGuildMembers()
print(format("%d guild members: %d online, %d offline", numTotal, numOnline, numTotal-numOnline))
</syntaxhighlight>

==Details==
* You may need to call [[API_C_GuildInfo.GuildRoster|C_GuildInfo.GuildRoster()]] first in order to obtain correct data. May return wrong values immediately after quitting a guild. Maximum returned value is 500.
* This returns values of this API seem to be no longer affected by {{api|t=a|SetGuildRosterShowOffline}})()

==Patch changes==
* {{Patch 10.2.0|note=Removed <code>numOnlineAndMobileMembers</code> return value.}}
```