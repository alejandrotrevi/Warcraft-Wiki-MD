# API C Commentator.GetTeamColor

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Commentator|system=CommentatorFrame}}
Needs summary.
 color = C_Commentator.GetTeamColor(teamIndex)
       = C_Commentator.GetTeamColorByUnit(unitToken)

==Arguments==
===<font color="#4ec9b0">GetTeamColor</font>===
:;teamIndex:{{apitype|number}}

===<font color="#4ec9b0">GetTeamColorByUnit</font>===
:;unitToken:{{apitype|string}} : [[UnitId]]

==Returns==
:;color:{{apitype|ColorMixin}}

==Patch changes==
* {{Patch 9.0.1|note=Changed to <code>C_Commentator.GetTeamColor()</code> and returns a mixin.}}
* {{Patch 7.3.5|note=Added as <code>C_Commentator.GetTeamHighlightColor()</code>}}
```