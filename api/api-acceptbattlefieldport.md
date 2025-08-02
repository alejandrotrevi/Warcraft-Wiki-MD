# API AcceptBattlefieldPort

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Enters the Battleground if the queue is ready.
 AcceptBattlefieldPort(index, accept)

==Arguments==
:;index:{{apitype|number}} - The battlefield in queue to enter.
:;accept:{{apitype|boolean}} - Whether or not to accept entry to the battlefield.

==Patch changes==
* {{Patch 4.1.0|note=Protected; requires a hardware event.}}
* {{Patch 1.9.0|note=Added ''index'' argument.<ref>{{ref FrameXML|StaticPopup.lua|1.9.0|4937|17|2006-01-03}}</ref>}}
* {{Patch 1.4.0|note=Added.<ref>{{ref FrameXML|BattlefieldFrame.lua|1.4.0|4341|239|2005-04-19}}</ref>}}

==References==
{{reflist}}
```