# API C Club.GetMessageInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 message = C_Club.GetMessageInfo(clubId, streamId, messageId)

==Arguments==
:;clubId:{{apitype|string}}
:;streamId:{{apitype|string}}
:;messageId:structure - ClubMessageIdentifier

{{:Struct_Club.ClubMessageIdentifier}}

==Returns==
:;message:structure - ClubMessageInfo (nilable)

{{:Struct_Club.ClubMessageInfo}}

==Details==
* Get info about a particular message.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```