# API C ScenarioInfo.GetScenarioStepInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ScenarioInfo|system=ScenarioInfo}}
Needs summary.
 scenarioStepInfo = C_ScenarioInfo.GetScenarioStepInfo([scenarioStepID])

==Arguments==
:;scenarioStepID:{{apitype|number?}}

==Returns==
:;scenarioStepInfo:{{apitype|ScenarioStepInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| title || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| numCriteria || {{apitype|number}} || 
|-
| stepFailed || {{apitype|boolean}} || 
|-
| isBonusStep || {{apitype|boolean}} || 
|-
| isForCurrentStepOnly || {{apitype|boolean}} || 
|-
| shouldShowBonusObjective || {{apitype|boolean}} || 
|-
| spells || {{apitype|ScenarioStepSpellInfo[]}} || 
|-
| weightedProgress || {{apitype|number?}} || 
|-
| rewardQuestID || {{apitype|number}} || 
|-
| widgetSetID || {{apitype|number?}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ ScenarioStepSpellInfo
! Field !! Type !! Description
|-
| spellID || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| icon || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```