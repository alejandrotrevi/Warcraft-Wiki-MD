# API C SocialQueue.GetGroupMembers

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 groupMembers = C_SocialQueue.GetGroupMembers(groupGUID)

==Arguments==
:;groupGUID:{{apitype|string}}

==Returns==
:;groupMembers:structure - SocialQueuePlayerInfo[]
{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| guid || {{apitype|string}} || 
|-
| clubId || {{apitype|string?}} || 
|}

==Patch changes==
* {{Patch 7.1.0|note=Added.}}
```