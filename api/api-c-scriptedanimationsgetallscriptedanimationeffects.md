# API C ScriptedAnimations.GetAllScriptedAnimationEffects

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ScriptedAnimations|system=ScriptedAnimations}}
Needs summary.
 scriptedAnimationEffects = C_ScriptedAnimations.GetAllScriptedAnimationEffects()

==Returns==
:;scriptedAnimationEffects:{{apitype|ScriptedAnimationEffect[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| id || {{apitype|number}} || 
|-
| visual || {{apitype|number}} || 
|-
| visualScale || {{apitype|number}} || 
|-
| duration || {{apitype|number}} || 
|-
| trajectory || {{apitype|Enum.ScriptedAnimationTrajectory}} || 
|-
| yawRadians || {{apitype|number}} || 
|-
| pitchRadians || {{apitype|number}} || 
|-
| rollRadians || {{apitype|number}} || 
|-
| offsetX || {{apitype|number}} || 
|-
| offsetY || {{apitype|number}} || 
|-
| offsetZ || {{apitype|number}} || 
|-
| animation || {{apitype|number}} || 
|-
| animationSpeed || {{apitype|number}} || 
|-
| alpha || {{apitype|number}} || 
|-
| useTargetAsSource || {{apitype|boolean}} || 
|-
| startBehavior || {{apitype|Enum.ScriptedAnimationBehavior?}} || 
|-
| startSoundKitID || {{apitype|number?}} || 
|-
| finishEffectID || {{apitype|number?}} || 
|-
| finishBehavior || {{apitype|Enum.ScriptedAnimationBehavior?}} || 
|-
| finishSoundKitID || {{apitype|number?}} || 
|-
| startAlphaFade || {{apitype|number?}} || 
|-
| startAlphaFadeDuration || {{apitype|number?}} || 
|-
| endAlphaFade || {{apitype|number?}} || 
|-
| endAlphaFadeDuration || {{apitype|number?}} || 
|-
| animationStartOffset || {{apitype|number?}} || 
|-
| loopingSoundKitID || {{apitype|number?}} || 
|-
| particleOverrideScale || {{apitype|number?}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.ScriptedAnimationTrajectory
! Value !! Field !! Description
|-
| 0 || AtSource || 
|-
| 1 || AtTarget || 
|-
| 2 || Straight || 
|-
| 3 || CurveLeft || 
|-
| 4 || CurveRight || 
|-
| 5 || CurveRandom || 
|-
| 6 || HalfwayBetween || 
|}

{{:Enum.ScriptedAnimationBehavior}}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>animation, alpha, useTargetAsSource, startAlphaFade, startAlphaFadeDuration, endAlphaFade, endAlphaFadeDuration, animationStartOffset, loopingSoundKitID, particleOverrideScale</code> fields.}}
* {{Patch 9.0.1|note=Added.}}
```