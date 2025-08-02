# API EJ IsValidInstanceDifficulty

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the difficultyID is valid for use in the journal.
 isValid = EJ_IsValidInstanceDifficulty(difficultyID)

==Arguments==
:;[[DifficultyID|difficultyID]]:{{apitype|number}} - the following IDs should be valid:

{| class="sortable darktable zebra"
|-
! ID !! Name !! Type
|-
| 1 || Normal || party
|-
| 2 || Heroic || party
|-
| 14 || Normal || raid
|-
| 15 || Heroic || raid
|-
| 16 || Mythic || raid
|-
| 17 || Looking For Raid || raid
|-
| 23 || Mythic || party
|-
| 24 || Timewalking || party
|-
| 33 || Timewalking || raid
|}

==Returns==
:;isValid:{{apitype|boolean}}

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|EJ_GetDifficulty}}
* {{api|EJ_SetDifficulty}}
```