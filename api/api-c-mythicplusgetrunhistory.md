# API C MythicPlus.GetRunHistory

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MythicPlus|system=MythicPlusInfo}}
Needs summary.
 runs = C_MythicPlus.GetRunHistory([includePreviousWeeks, includeIncompleteRuns])

==Arguments==
:;includePreviousWeeks:{{apitype|boolean?|default=false}}
:;includeIncompleteRuns:{{apitype|boolean?|default=false}}

==Returns==
:;runs:{{apitype|MythicPlusRunInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| mapChallengeModeID || {{apitype|number}} || {{dbc|mapchallengemode|MapChallengeMode.ID}}
|-
| level || {{apitype|number}} || 
|-
| thisWeek || {{apitype|boolean}} || 
|-
| completed || {{apitype|boolean}} || 
|-
| runScore || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>runScore</code> field.}}
* {{Patch 9.0.1|note=Added.}}
```