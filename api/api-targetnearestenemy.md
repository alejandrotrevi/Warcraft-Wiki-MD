# API TargetNearestEnemy

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=TargetScript}} {{restrictedapi|protected|note=Use the [[MACRO targetenemy|/targetenemy]] slash command.}}
Selects the nearest enemy as the current target.
 TargetNearestEnemy([reverse])

==Arguments==
:;reverse:{{apitype|boolean}} - true to cycle backwards; false to cycle forwards.

==Details==
* This is bound to the tab key by default.
* This function only works if initiated by a hardware event.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
```