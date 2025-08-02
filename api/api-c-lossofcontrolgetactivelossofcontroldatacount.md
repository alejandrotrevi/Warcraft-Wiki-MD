# API C LossOfControl.GetActiveLossOfControlDataCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LossOfControl|system=LossOfControl}}
Returns the number of active loss-of-control effects.
 count = C_LossOfControl.GetActiveLossOfControlDataCount()
       = C_LossOfControl.GetActiveLossOfControlDataCountByUnit(unitToken)

==Arguments==
===<font color="#4ec9b0">GetActiveLossOfControlDataCount</font>===
:None

===<font color="#4ec9b0">GetActiveLossOfControlDataCountByUnit</font>===
:;unitToken:{{apitype|string}} : [[UnitId]] - Only works while in commentator mode.

==Returns==
:;count:{{apitype|number}}

==Patch changes==
* {{Patch 9.0.1|note=Changed to <code>C_LossOfControl.GetActiveLossOfControlDataCount()</code>}}
* {{Patch 5.1.0|note=Added as {{api|C_LossOfControl.GetNumEvents}}()}}
```