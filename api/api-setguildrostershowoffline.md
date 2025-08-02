# API SetGuildRosterShowOffline

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
{{Ambox
| image = [[Image:spell_holy_borrowedtime.png|48px]]
| border = red
| type = This API no longer seems to do anything and is unused in (mainline) FrameXML.
}}
<!--desc-->Sets the show offline guild members flag.
 SetGuildRosterShowOffline(enabled)

==Arguments==
:;enabled:{{apitype|boolean}} - True includes all guild members; false filters out offline guild members.

==Details==
* Triggers {{api|t=e|GUILD_ROSTER_UPDATE}} if filtering mode has changed -- facilitating a customary call to {{api|GuildRoster()}} if this event is registered.

==Example==
<syntaxhighlight lang="lua>
-- Fetch updated info when required
local f = CreateFrame("Frame")
f:RegisterEvent("GUILD_ROSTER_UPDATE")
f:HookScript("OnEvent", function(event)
	if (event == "GUILD_ROSTER_UPDATE") then
		GuildRoster()
	end
end)

-- At some point later point in your code...
SetGuildRosterShowOffline(false)
</syntaxhighlight>
```