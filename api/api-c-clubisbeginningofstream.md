# API C Club.IsBeginningOfStream

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 isBeginningOfStream = C_Club.IsBeginningOfStream(clubId, streamId, messageId)

==Arguments==
:;clubId:{{apitype|string}}
:;streamId:{{apitype|string}}
:;messageId:structure - ClubMessageIdentifier

{{:Struct_Club.ClubMessageIdentifier}}

==Returns==
:;isBeginningOfStream:{{apitype|boolean}}

==Details==
* Returns whether the given message is the first message in the stream, taking into account ignored messages

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```