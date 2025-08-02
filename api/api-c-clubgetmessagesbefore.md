# API C Club.GetMessagesBefore

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 messages = C_Club.GetMessagesBefore(clubId, streamId, newest, count)

==Arguments==
:;clubId:{{apitype|string}}
:;streamId:{{apitype|string}}
:;newest:structure - ClubMessageIdentifier
:;count:{{apitype|number}}

{{:Struct_Club.ClubMessageIdentifier}}

==Returns==
:;messages:structure - ClubMessageInfo[]

{{:Struct_Club.ClubMessageInfo}}

==Details==
* Get downloaded messages before (and including) the specified messageId limited by count. These are filtered by ignored players

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```