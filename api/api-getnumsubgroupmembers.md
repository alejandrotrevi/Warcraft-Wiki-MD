# API GetNumSubgroupMembers

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of other players in the party or raid subgroup.
 numSubgroupMembers = GetNumSubgroupMembers([groupType])

==Arguments==
:;groupType:{{apitype|number?}}
{{:LE_PARTY_CATEGORY|nocaption=1}}

==Returns==
:;numSubgroupMembers:{{apitype|number}} - number of players in the player's sub-group, excluding the player.

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|GetNumGroupMembers}} }}
{{apirow | Related Events | {{api|t=e|GROUP_ROSTER_UPDATE}} }}
|}

==Patch changes==
* {{Patch 5.0.4|note=Replaced {{api|GetNumPartyMembers}} and {{api|GetRealNumPartyMembers}}.}}
```