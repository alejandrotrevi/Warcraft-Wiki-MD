# API C LossOfControl.GetActiveLossOfControlData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LossOfControl|system=LossOfControl}}
Returns info about an active loss-of-control effect.
 event = C_LossOfControl.GetActiveLossOfControlData(index)
       = C_LossOfControl.GetActiveLossOfControlDataByUnit(unitToken, index)

==Arguments==
===<font color="#4ec9b0">GetActiveLossOfControlData</font>===
:;index:{{apitype|number}} - Ranging from 1 to {{api|C_LossOfControl.GetActiveLossOfControlDataCount}}()

===<font color="#4ec9b0">GetActiveLossOfControlDataByUnit</font>===
:;unitToken:{{apitype|string}} : [[UnitId]] - Only works while in commentator mode.
:;index:{{apitype|number}}

==Returns==
:;event:{{apitype|LossOfControlData?}}
{{:Struct LossOfControlData|nocaption=1}}

==Details==
* Loss of Control debuffs that are applied only while standing in an Area of Effect may not include a startTime, timeRemaining nor duration in the table returned. An example of this is [[Vol'zith the Whisperer]]'s [https://www.wowhead.com/spell=269419 Yawning Gate] ability.

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_LossOfControl.GetActiveLossOfControlData()</code>}}
* {{Patch 5.1.0|note=Added as {{api|C_LossOfControl.GetEventInfo}}()}}
```