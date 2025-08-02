# API C PlayerMentorship.GetMentorshipStatus

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PlayerMentorship|system=PlayerMentorship}}
Needs summary.
 status = C_PlayerMentorship.GetMentorshipStatus(playerLocation)

==Arguments==
:;playerLocation:{{apitype|PlayerLocationMixin}}

==Returns==
:;status:{{apitype|Enum.PlayerMentorshipStatus}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| align="center" | 0 || None || 
|-
| align="center" | 1 || Newcomer || 
|-
| align="center" | 2 || Mentor || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```