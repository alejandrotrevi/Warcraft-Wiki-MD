# API C Club.GetMessagesInRange

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Club|system=Club}}
Get downloaded messages in the given range.
 messages = C_Club.GetMessagesInRange(clubId, streamId, oldest, newest)

==Arguments==
:;clubId:{{apitype|string}}
:;streamId:{{apitype|string}}
:;oldest:{{apitype|ClubMessageIdentifier}}
:;newest:{{apitype|ClubMessageIdentifier}}
{{:Struct ClubMessageIdentifier|nocaption=1}}

==Returns==
:;messages:{{apitype|ClubMessageInfo[]}}
{{:Struct ClubMessageInfo|nocaption=1}}

==Details==
* The messages are filtered by ignored players

==Example==
<onlyinclude>[[File:API C Club.GetMessagesInRange.png|right]]
* Prints all guild messages from start to end. Only tested with a small guild.
<syntaxhighlight lang="lua">
local club = C_Club.GetGuildClubId()
local streams = C_Club.GetStreams(club)
local guildStream = streams[1].streamId
local ranges = C_Club.GetMessageRanges(club, guildStream)
local oldest, newest = ranges[1].oldestMessageId, ranges[1].newestMessageId
local messages = C_Club.GetMessagesInRange(club, guildStream, oldest, newest)
for _, v in pairs(messages) do
	local timestamp = date("%Y-%m-%d %H:%M:%S", v.messageId.epoch/1e6)
	print(format("%s %s: |cffdda0dd%s|r", timestamp, v.author.name, v.content))
end
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```