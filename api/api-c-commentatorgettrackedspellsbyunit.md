# API C Commentator.GetTrackedSpellsByUnit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Commentator|system=CommentatorFrame}}
Needs summary.
 spells = C_Commentator.GetTrackedSpellsByUnit(unitToken, category)

==Arguments==
:;unitToken:{{apitype|string}} : [[UnitId]]
:;category:{{apitype|Enum.TrackedSpellCategory}}
{{:Enum.TrackedSpellCategory|nocaption=1}}

==Returns==
:;spells:{{apitype|number[]?}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```