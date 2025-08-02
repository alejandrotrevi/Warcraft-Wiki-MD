# API C ModelInfo.GetModelSceneCameraInfoByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ModelInfo|system=ModelInfo}}
Needs summary.
 modelSceneCameraInfo = C_ModelInfo.GetModelSceneCameraInfoByID(modelSceneCameraID)

==Arguments==
:;modelSceneCameraID:{{apitype|number}}

==Returns==
:;modelSceneCameraInfo:{{apitype|UIModelSceneCameraInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| modelSceneCameraID || {{apitype|number}} || 
|-
| scriptTag || {{apitype|string}} || 
|-
| cameraType || {{apitype|string}} || 
|-
| target || {{apitype|Vector3DMixin}} || 
|-
| yaw || {{apitype|number}} || 
|-
| pitch || {{apitype|number}} || 
|-
| roll || {{apitype|number}} || 
|-
| zoomDistance || {{apitype|number}} || 
|-
| minZoomDistance || {{apitype|number}} || 
|-
| maxZoomDistance || {{apitype|number}} || 
|-
| zoomedTargetOffset || {{apitype|Vector3DMixin}} || 
|-
| zoomedYawOffset || {{apitype|number}} || 
|-
| zoomedPitchOffset || {{apitype|number}} || 
|-
| zoomedRollOffset || {{apitype|number}} || 
|-
| flags || {{apitype|Enum.ModelSceneSetting}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.ModelSceneSetting
! Value !! Field !! Description
|-
| 1 || AlignLightToOrbitDelta || 
|}

==Patch changes==
* {{Patch 7.3.5|note=Added <code>flags</code> field.}}
* {{Patch 7.2.0|note=Added.}}
```