# API C QuestSession.GetSessionBeginDetails

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Identifies the party member requesting [[Party Sync]].
 details = C_QuestSession.GetSessionBeginDetails()

==Returns==
:;details:{{api|t=i?|Struct QuestSession.QuestSessionPlayerDetails|nil=Returns nil if there is no pending request from another party member.}}
{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| guid || {{apitype|string}} || [[GUID]] 
|}

==Details==
* This only applies when a pending request was intitiated by another party member.

==Patch changes==
* {{Patch 8.2.5|note=Added.<ref>{{ref FrameXML|QuestSession.lua|8.2.5|31960||20190924}}</ref>}}

==See also==
* {{api|C_QuestSession.SendSessionBeginResponse(beginSession)}} - Used to indicate agreement with starting Party Sync.

==References==
{{Reflist}}
```