# API C ScenarioInfo.GetScenarioInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ScenarioInfo|system=ScenarioInfo}}
Needs summary.
 scenarioInfo = C_ScenarioInfo.GetScenarioInfo()

==Returns==
:;scenarioInfo:{{apitype|ScenarioInformation}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| currentStage || {{apitype|number}} || 
|-
| numStages || {{apitype|number}} || 
|-
| flags || {{apitype|number}} || 
|-
| isComplete || {{apitype|boolean}} || 
|-
| xp || {{apitype|number}} || 
|-
| money || {{apitype|number}} || 
|-
| type || {{apitype|number}} || 
|-
| area || {{apitype|string}} || 
|-
| uiTextureKit || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```