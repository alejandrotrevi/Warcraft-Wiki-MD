# API C GossipInfo.GetFriendshipReputation

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Needs summary.
 reputationInfo = C_GossipInfo.GetFriendshipReputation(friendshipFactionID)

==Arguments==
:;friendshipFactionID:{{apitype|number}}

==Returns==
:;reputationInfo:{{apitype|FriendshipReputationInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| friendshipFactionID || {{apitype|number}} || 
|-
| standing || {{apitype|number}} || 
|-
| maxRep || {{apitype|number}} || 
|-
| name || {{apitype|string?}} || 
|-
| text || {{apitype|string}} || 
|-
| texture || {{apitype|number}} || 
|-
| reaction || {{apitype|string}} || 
|-
| reactionThreshold || {{apitype|number}} || 
|-
| nextThreshold || {{apitype|number?}} || 
|-
| reversedColor || {{apitype|boolean}} || 
|-
| overrideColor || {{apitype|number?}} || 
|}
```