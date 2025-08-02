# API C ChallengeMode.GetGuildLeaders

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 topAttempt = C_ChallengeMode.GetGuildLeaders()

==Returns==
:;topAttempt:structure - ChallengeModeGuildTopAttempt[]

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| classFileName || {{apitype|string}} || 
|-
| keystoneLevel || {{apitype|number}} || 
|-
| mapChallengeModeID || {{apitype|number}} || 
|-
| isYou || {{apitype|boolean}} || 
|-
| members || structure ChallengeModeGuildAttemptMember[] || 
|}

{| class="sortable darktable zebra"
|+ ChallengeModeGuildAttemptMember
|-
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| classFileName || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```