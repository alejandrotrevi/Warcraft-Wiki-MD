# API C ModelInfo.GetModelSceneActorInfoByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ModelInfo|system=ModelInfo}}
Needs summary.
 actorInfo = C_ModelInfo.GetModelSceneActorInfoByID(modelActorID)

==Arguments==
:;modelActorID:{{apitype|number}}

==Returns==
:;actorInfo:{{apitype|UIModelSceneActorInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| modelActorID || {{apitype|number}} || 
|-
| scriptTag || {{apitype|string}} || 
|-
| position || {{apitype|Vector3DMixin}} || 
|-
| yaw || {{apitype|number}} || 
|-
| pitch || {{apitype|number}} || 
|-
| roll || {{apitype|number}} || 
|-
| normalizeScaleAggressiveness || {{apitype|number?}} || 
|-
| useCenterForOriginX || {{apitype|boolean}} || 
|-
| useCenterForOriginY || {{apitype|boolean}} || 
|-
| useCenterForOriginZ || {{apitype|boolean}} || 
|-
| modelActorDisplayID || {{apitype|number?}} || 
|}

==Patch changes==
* {{Patch 7.2.0|note=Added.}}
```