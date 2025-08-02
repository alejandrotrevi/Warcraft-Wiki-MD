# API MoveForwardStart

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent}}
The player begins moving forward at the specified time.
 MoveForwardStart(startTime)

==Arguments==
:;startTime:{{apitype|number}} - Begin moving forward at this time, per {{api|GetTime}} * 1000.

==Details==
* As of 1.6, the time parameter seems to be ignored, and this function needs to be called as the result of a button press.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
* {{Patch 1.6.0|note=Now requires a hardware event.}}
```