# API C Commentator.GetPlayerData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Commentator|system=CommentatorFrame}}
Needs summary.
 info = C_Commentator.GetPlayerData(teamIndex, playerIndex)

==Arguments==
:;teamIndex:{{apitype|number}}
:;playerIndex:{{apitype|number}}

==Returns==
:;info:{{apitype|CommentatorPlayerData?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| unitToken || {{apitype|string}} || 
|-
| name || {{apitype|string}} || 
|-
| faction || {{apitype|number}} || 
|-
| specialization || {{apitype|number}} || 
|-
| damageDone || {{apitype|number}} || 
|-
| damageTaken || {{apitype|number}} || 
|-
| healingDone || {{apitype|number}} || 
|-
| healingTaken || {{apitype|number}} || 
|-
| kills || {{apitype|number}} || 
|-
| deaths || {{apitype|number}} || 
|-
| soloShuffleRoundWins || {{apitype|number}} || 
|-
| soloShuffleRoundLosses || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 9.2.0|note=Added <code>soloShuffleRoundLosses, soloShuffleRoundWins</code> returns.}}
* {{Patch 9.0.1|note=Changed to <code>C_Commentator.GetPlayerData()</code> and returns structured data.}}
* {{Patch 6.1.0|note=Added as <code>C_Commentator.GetPlayerInfo()</code>}}
```