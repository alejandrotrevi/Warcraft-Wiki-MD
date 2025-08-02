# API C Club.GetInvitationCandidates

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Club|system=Club}}
Returns a list of players that you can send a request to a Battle.net club. Returns an empty list for Character based clubs
 candidates = C_Club.GetInvitationCandidates(filter?, maxResults?, cursorPosition?, allowFullMatch?, clubId)

==Arguments==
:;filter:{{apitype|string?}}
:;maxResults:{{apitype|number?}}
:;cursorPosition:{{apitype|number?}}
:;allowFullMatch:{{apitype|boolean?}}
:;clubId:{{apitype|string}}

==Returns==
:;candidates:{{apitype|ClubInvitationCandidateInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| memberId || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| priority || {{apitype|number}} || 
|-
| status || {{apitype|Enum.ClubInvitationCandidateStatus}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.ClubInvitationCandidateStatus
! Value !! Field !! Description
|-
| 0 || Available || 
|-
| 1 || InvitePending || 
|-
| 2 || AlreadyMember || 
|}

==Patch changes==
* {{Patch 8.1.0|note=Added <code>allowFullMatch</code> argument.}}
* {{Patch 8.0.1|note=Added.}}
```