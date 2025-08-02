# API C QuestSession.CanStop

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Indicates the player may request stopping [[Party Sync]].
 allowed = C_QuestSession.CanStop()

==Returns==
:;allowed:{{apitype|boolean}} - True if the player is in a party with Party Sync but may end it.

==Patch changes==
* {{Patch 8.2.5|note=Added.<ref>{{ref FrameXML|QuestSession.lua|8.2.5|31960||20190924}}</ref>}}

==See also==
* {{api|C_QuestSession.CanStart()}} - Applicable before Party Sync has begun.
* {{api|C_QuestSession.RequestSessionStop()}} - Used to terminate Party Sync, if CanStop() is true.

==References==
{{Reflist}}
```