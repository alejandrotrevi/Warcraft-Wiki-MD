# API GetBattlegroundPoints

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
[NYI] Returns battlegrounds points earned by a team.
 currentPoints, maxPoints = GetBattlegroundPoints(team)

==Arguments==
:;team:{{apitype|number}} - team to query the points of; 0 for Horde, 1 for Alliance.

==Returns==
:;currentPoints:{{apitype|number}} - current battleground points earned by the team.
:;maxPoints:{{apitype|number}} - maximum amount of battleground points the team can earn.

==Details==
* As of 5.3, both return values are always 0; FrameXML comments in <code>WorldStateFrame.lua</code> state:
*: ''Long-term we'd like the battleground objectives to work more like this, but it's not working for 5.3''

==Patch changes==
* {{Patch 5.3.0|note=Added; non-functional.}}
```