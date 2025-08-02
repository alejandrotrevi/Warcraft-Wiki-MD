# API C Club.EditStream

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 C_Club.EditStream(clubId, streamId [, name [, subject [, leadersAndModeratorsOnly]]])

==Arguments==
:;clubId:{{apitype|string}}
:;streamId:{{apitype|string}}
:;name:{{apitype|string?}}
:;subject:{{apitype|string?}}
:;leadersAndModeratorsOnly:{{apitype|boolean?}}

==Details==
* Check the canSetStreamName, canSetStreamSubject, canSetStreamAccess privileges. nil arguments will not change existing stream data.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```