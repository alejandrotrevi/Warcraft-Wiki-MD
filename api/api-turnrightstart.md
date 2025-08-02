# API TurnRightStart

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent}}
Turns the player right at the specified time.
 TurnRightStart(startTime)

==Arguments==
:;startTime:{{apitype|number}} - Begin turning right at this time, per {{api|GetTime}} * 1000

==Details==
* As of 1.6, the time parameter seems to be ignored, and this function needs to be called as the result of a button press.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
* {{Patch 1.6.0|note=Now requires a hardware event.}}
```