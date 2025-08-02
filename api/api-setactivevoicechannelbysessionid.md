# API SetActiveVoiceChannelBySessionID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Set the active voice channel.
 success = SetActiveVoiceChannelBySessionID(id)

==Arguments==
:;id:{{apitype|Number}} - Channel ID.

==Returns==
:;success:{{apitype|boolean}} - Whether the channel changed to to the given ID.

==Details==
* Triggers {{api|t=e|VOICE_SESSIONS_UPDATE}} if the active channel switches.
* This function is not applicable to "World" channels such as Trade and LookingForGroup.
* IDs are not constant; they are assigned as the client joins each channel so they will change for users who have joined a variable number of channels.  Refer to {{api|GetNumVoiceSessions()}} and {{api|GetVoiceSessionInfo()}}.

==Example==
Simple usage:
<syntaxhighlight lang="lua">
local success = SetActiveVoiceChannelBySessionID(2)
print(success)		-- true
</syntaxhighlight>

Finding a channel's ID and then joining it:
<syntaxhighlight lang="lua">
function SetChannelIDByName(name)
	for id=1, GetNumVoiceSessions() do
		if name == GetVoiceSessionInfo(id) then
			return SetActiveVoiceChannelBySessionID(id)
		end
	end
end
</syntaxhighlight>
```