# API C Club.GetStreams

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 streams = C_Club.GetStreams(clubId)

==Arguments==
:;clubId:{{apitype|string}}

==Returns==
:;streams:structure - ClubStreamInfo[]

{{:Struct_Club.ClubStreamInfo}}

==Example==
* Prints the streams/channels for your guild.
<syntaxhighlight lang="lua">
local club = C_Club.GetGuildClubId()
local streams = C_Club.GetStreams(club)
for _, v in pairs(streams) do
	print(v.streamId, v.name)
end

-- 1, "Guild"
-- 2, "Officer"
</syntaxhighlight>

{{:API_C_Club.GetMessagesInRange}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```