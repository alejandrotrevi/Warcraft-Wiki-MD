# API GetUnitChargedPowerPoints

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns a table of indices for combo points that have been charged. 
 pointIndices = GetUnitChargedPowerPoints(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;pointIndices:{{apitype|number[]}} - An array of 1-based indices of animacharged combo points, e.g. <code style="white-space:nowrap;">{ [1] = 2 }</code> means the second combo point is charged.

==Details==
* May return nil if if the unit has no combo points, or none are charged.

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```