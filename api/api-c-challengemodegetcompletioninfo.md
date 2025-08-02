# API C ChallengeMode.GetCompletionInfo

**Contributor:** Lansmi

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ChallengeMode|system=ChallengeModeInfo}}
{{deprecatedapi|patch=11.0.5}}
Needs summary.
 mapChallengeModeID, level, time, onTime, keystoneUpgradeLevels, practiceRun,
  oldOverallDungeonScore, newOverallDungeonScore, IsMapRecord, IsAffixRecord,
  PrimaryAffix, isEligibleForScore, members
     = C_ChallengeMode.GetCompletionInfo()

==Returns==
:;mapChallengeModeID:{{apitype|number}}
:;level:{{apitype|number}}
:;time:{{apitype|number}} - Time in milliseconds.
:;onTime:{{apitype|boolean}}
:;keystoneUpgradeLevels:{{apitype|number}}
:;practiceRun:{{apitype|boolean}}
:;oldOverallDungeonScore:{{apitype|number}}
:;newOverallDungeonScore:{{apitype|number}}
:;IsMapRecord:{{apitype|boolean}}
:;IsAffixRecord:{{apitype|boolean}}
:;PrimaryAffix:{{apitype|number}}
:;isEligibleForScore:{{apitype|boolean}}
:;members:{{apitype|ChallengeModeCompletionMemberInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| memberGUID || {{apitype|string}} || 
|-
| name || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 9.1.5|note=Added <code>isEligibleForScore</code> return.}}
* {{Patch 9.1.0|note=Added <code>oldOverallDungeonScore, newOverallDungeonScore, IsMapRecord, IsAffixRecord, PrimaryAffix, members</code> returns.}}
* {{Patch 8.2.0|note=Added <code>practiceRun</code> return.}}
* {{Patch 7.2.0|note=Added.}}
```