# API C Club.GetAvatarIdList

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 avatarIds = C_Club.GetAvatarIdList(clubType)

==Arguments==
:;clubType:Enum.ClubType

{{:Enum_Club.ClubType}}

==Returns==
:;avatarIds:{{apitype|number[]?}}

==Details==
* listen for AVATAR_LIST_UPDATED event. This can happen if we haven't downloaded the battle.net avatar list yet

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```