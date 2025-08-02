# API C Club.GetInvitationsForClub

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 invitations = C_Club.GetInvitationsForClub(clubId)

==Arguments==
:;clubId:{{apitype|string}}

==Returns==
:;invitations:structure - ClubInvitationInfo[]

{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| invitationId || {{apitype|string}} || 
|-
| isMyInvitation || {{apitype|boolean}} || 
|-
| invitee || structure ClubMemberInfo || 
|}

{{:Struct_Club.ClubMemberInfo}}

==Details==
* Get the pending invitations for this club. Call RequestInvitationsForClub() to retrieve invitations from server.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```