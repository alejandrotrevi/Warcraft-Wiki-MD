# API C QuestSession.CanStart

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Indicates the player may request starting [[Party Sync]].
 allowed = C_QuestSession.CanStart()

==Returns==
:;allowed:{{apitype|boolean}} - True if the player is in a party that has not yet begun to activate Party Sync.

==Patch changes==
* {{Patch 8.2.5|note=Added.<ref>{{ref FrameXML|QuestSession.lua|8.2.5|31960||20190924}}</ref>}}

==See also==
* {{api|C_QuestSession.CanStop()}} - Applicable after Party Sync has begun.
* {{api|C_QuestSession.RequestSessionStart()}} - Used to request Party Sync, if CanStart() is true.

==References==
{{Reflist}}
```