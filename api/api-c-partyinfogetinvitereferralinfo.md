# API C PartyInfo.GetInviteReferralInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for Quick join invites.
 outReferredByGuid, outReferredByName, outRelationType, outIsQuickJoin, outClubId = C_PartyInfo.GetInviteReferralInfo(inviteGUID)

==Arguments==
:;inviteGUID:{{apitype|string}}

==Returns==
:;outReferredByGuid:{{apitype|string}}
:;outReferredByName:{{apitype|string}}
:;outRelationType:Enum.PartyRequestJoinRelation
:;outIsQuickJoin:{{apitype|boolean}}
:;outClubId:{{apitype|string}}

{| class="sortable darktable zebra"
|+ Enum.PartyRequestJoinRelation
|-
! Value !! Field !! Description
|-
| <center>0</center> || None ||
|-
| <center>1</center> || Friend ||
|-
| <center>2</center> || Guild ||
|-
| <center>3</center> || Club ||
|-
| <center>4</center> || NumPartyRequestJoinRelations ||
|}

==Patch changes==
* {{Patch 8.1.0|note=Moved to {{api|C_PartyInfo.GetInviteReferralInfo}}. The previous alias is deprecated. [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#194]}}
* {{Patch 7.1.0|note=Added as {{api|GetInviteReferralInfo}}.}}
```