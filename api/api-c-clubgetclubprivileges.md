# API C Club.GetClubPrivileges

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 privilegeInfo = C_Club.GetClubPrivileges(clubId)

==Arguments==
:;clubId:{{apitype|string}}

==Returns==
:;privilegeInfo:structure - ClubPrivilegeInfo

{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| canDestroy || {{apitype|boolean}} || 
|-
| canSetAttribute || {{apitype|boolean}} || 
|-
| canSetName || {{apitype|boolean}} || 
|-
| canSetDescription || {{apitype|boolean}} || 
|-
| canSetAvatar || {{apitype|boolean}} || 
|-
| canSetBroadcast || {{apitype|boolean}} || 
|-
| canSetPrivacyLevel || {{apitype|boolean}} || 
|-
| canSetOwnMemberAttribute || {{apitype|boolean}} || 
|-
| canSetOtherMemberAttribute || {{apitype|boolean}} || 
|-
| canSetOwnMemberNote || {{apitype|boolean}} || 
|-
| canSetOtherMemberNote || {{apitype|boolean}} || 
|-
| canSetOwnVoiceState || {{apitype|boolean}} || 
|-
| canSetOwnPresenceLevel || {{apitype|boolean}} || 
|-
| canUseVoice || {{apitype|boolean}} || 
|-
| canVoiceMuteMemberForAll || {{apitype|boolean}} || 
|-
| canGetInvitation || {{apitype|boolean}} || 
|-
| canSendInvitation || {{apitype|boolean}} || 
|-
| canSendGuestInvitation || {{apitype|boolean}} || 
|-
| canRevokeOwnInvitation || {{apitype|boolean}} || 
|-
| canRevokeOtherInvitation || {{apitype|boolean}} || 
|-
| canGetBan || {{apitype|boolean}} || 
|-
| canGetSuggestion || {{apitype|boolean}} || 
|-
| canSuggestMember || {{apitype|boolean}} || 
|-
| canGetTicket || {{apitype|boolean}} || 
|-
| canCreateTicket || {{apitype|boolean}} || 
|-
| canDestroyTicket || {{apitype|boolean}} || 
|-
| canAddBan || {{apitype|boolean}} || 
|-
| canRemoveBan || {{apitype|boolean}} || 
|-
| canCreateStream || {{apitype|boolean}} || 
|-
| canDestroyStream || {{apitype|boolean}} || 
|-
| canSetStreamPosition || {{apitype|boolean}} || 
|-
| canSetStreamAttribute || {{apitype|boolean}} || 
|-
| canSetStreamName || {{apitype|boolean}} || 
|-
| canSetStreamSubject || {{apitype|boolean}} || 
|-
| canSetStreamAccess || {{apitype|boolean}} || 
|-
| canSetStreamVoiceLevel || {{apitype|boolean}} || 
|-
| canCreateMessage || {{apitype|boolean}} || 
|-
| canDestroyOwnMessage || {{apitype|boolean}} || 
|-
| canDestroyOtherMessage || {{apitype|boolean}} || 
|-
| canEditOwnMessage || {{apitype|boolean}} || 
|-
| canPinMessage || {{apitype|boolean}} || 
|-
| kickableRoleIds || {{apitype|number[]}} || Roles that can be kicked and banned
|}

==Details==
* The privileges for the logged in user for this club

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```