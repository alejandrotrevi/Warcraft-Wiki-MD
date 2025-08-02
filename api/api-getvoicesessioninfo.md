# API GetVoiceSessionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__

Returns name of the voice session of the given id. 
 sessionName, success = GetVoiceSessionInfo(id)

==Arguments==
:;id:{{apitype|number}} - id of the voice session.

==Returns==
:sessionName, success  <!-- remove this line if it's just one value -->

:;sessionName:Name of the voice session (channel name).
:;success:Returns 1 if the function was successful.

==Example==
 local sessionName, success = GetVoiceSessionInfo(1)

<big>'''Result'''</big>
 sessionName = "Party"
 success = 1

==Details==

: Does not return names of voice channels under the 'World' category (in the Voice Chat window). Use [[API GetChannelDisplayInfo|GetChannelDisplayInfo]] for that.
```