# API C QuestSession.SendSessionBeginResponse

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Consents to activating [[Party Sync]] following a request by another party member.
 C_QuestSession.SendSessionBeginResponse(beginSession)

==Arguments==
:;beginSession:{{apitype|boolean}} - True to agree with starting Party Sync, or false to reject it.

==Details==
* This only applies when a pending request was intitiated by another party member.

==Patch changes==
* {{Patch 8.2.5|note=Added.<ref>{{ref FrameXML|QuestSession.lua|8.2.5|31960||20190924}}</ref>}}

==See also==
* {{api|C_QuestSession.GetSessionBeginDetails()}} - Indicates which party member asked for the Party Sync to begin.

==References==
{{Reflist}}
```