# API GetCraftInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
 craftName, craftSubSpellName, craftType, numAvailable, isExpanded, trainingPointCost, requiredLevel = GetCraftInfo(index)

==Parameters==
===Arguments===
:;index:{{apitype|number}} - 1 to [[API GetNumCrafts|GetNumCrafts()]]

===Returns===
:;craftName:Name of the item you can craft

:;craftSubSpellName

:;craftType:{{apitype|string}} - "header" or how hard it is to create the item; trivial, easy, medium or optimal.

:;numAvailable:This is the number of items you can create with the reagents you have in your inventory (the number is also shown in the UI).

:;isExpanded:Only applies to headers. Indicates whether they are expanded or contracted.  Nil if not applicable.

:;trainingPointCost:This is the number of training points needed to train this skill if at a trainer. Nil if the craft window is not a trainer.

:;requiredLevel:The required level to train this skill if at a trainer. Nil if the craft window is not a trainer.

==Patch changes==
* {{Patch 3.0.2|note=Removed.}}
```