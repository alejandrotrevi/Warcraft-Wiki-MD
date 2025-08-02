# API C ModelInfo.GetModelSceneActorDisplayInfoByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ModelInfo|system=ModelInfo}}
Needs summary.
 actorDisplayInfo = C_ModelInfo.GetModelSceneActorDisplayInfoByID(modelActorDisplayID)

==Arguments==
:;modelActorDisplayID:{{apitype|number}}

==Returns==
:;actorDisplayInfo:{{apitype|UIModelSceneActorDisplayInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| animation || {{apitype|number}} || 
|-
| animationVariation || {{apitype|number}} || 
|-
| animSpeed || {{apitype|number}} || 
|-
| animationKitID || {{apitype|number?}} || 
|-
| spellVisualKitID || {{apitype|number?}} || 
|-
| alpha || {{apitype|number}} || 
|-
| scale || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Returns structured data.}}
* {{Patch 7.2.0|note=Added.}}
```