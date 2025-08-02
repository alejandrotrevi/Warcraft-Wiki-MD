# API C QuestSession.Exists

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Indiciates [[Party Sync]] is active or requested by a party member.
 exists = C_QuestSession.Exists()

==Returns==
:;exists:{{apitype|boolean}} - True if Party Sync is active or there is a pending request to activate it; false otherwise.

==Patch changes==
* {{Patch 8.2.5|note=Added.<ref>{{ref FrameXML|QuestSession.lua|8.2.5|31960||20190924}}</ref>}}

==See also==
* {{api|C_QuestSession.HasJoined()}} - Only true when active (excludes pending requests).

==References==
{{Reflist}}
```