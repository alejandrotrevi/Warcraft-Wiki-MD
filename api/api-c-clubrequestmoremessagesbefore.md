# API C Club.RequestMoreMessagesBefore

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 alreadyHasMessages = C_Club.RequestMoreMessagesBefore(clubId, streamId [, messageId, count])

==Arguments==
:;clubId:{{apitype|string}}
:;streamId:{{apitype|string}}
:;messageId:structure - ClubMessageIdentifier (optional)
{{:Struct_Club.ClubMessageIdentifier}}
:;count:{{apitype|number?}}

==Returns==
:;alreadyHasMessages:{{apitype|boolean}}

==Details==
* Call this when the user scrolls near the top of the message view, and more need to be displayed. The history will be downloaded backwards (newest to oldest).

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```