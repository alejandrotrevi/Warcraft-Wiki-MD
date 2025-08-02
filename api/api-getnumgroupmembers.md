# API GetNumGroupMembers

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of players in the group.
 numMembers = GetNumGroupMembers([groupType])

==Arguments==
:;groupType:{{apitype|number?}}
{{:LE_PARTY_CATEGORY|nocaption=1}}

==Returns==
:;numMembers:{{apitype|number}} - total number of players in the group (either party or raid), 0 if not in a group.

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|GetNumSubgroupMembers}} }}
{{apirow | Related Events | {{api|t=e|GROUP_ROSTER_UPDATE}} }}
|}

==Patch changes==
* {{Patch 5.0.4|note=Replaced {{api|GetNumRaidMembers}} and {{api|GetRealNumRaidMembers}}.}}
```