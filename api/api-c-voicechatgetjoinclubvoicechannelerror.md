# API C VoiceChat.GetJoinClubVoiceChannelError

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_VoiceChat|system=VoiceChat}}
Needs summary.
 errorReason = C_VoiceChat.GetJoinClubVoiceChannelError(clubId)

==Arguments==
:;clubId:{{apitype|string}}

==Returns==
:;errorReason:{{apitype|Enum.VoiceChannelErrorReason?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| align="center" | 0 || Unknown || 
|-
| align="center" | 1 || IsBattleNetChannel || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```