# API GetMirrorTimerProgress

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current value of the mirror timer.
 value = GetMirrorTimerProgress(timer)

==Arguments==
:;timer:{{apitype|string}} - the first return value from {{api|GetMirrorTimerInfo}}, identifying the timer queried. Valid values include "EXHAUSTION", "BREATH" and "FEIGNDEATH". 

==Return values==
:;value:{{apitype|number}} - current value of the timer. If the timer is not active, 0 is returned.

==See also==
* {{api|GetMirrorTimerInfo}}
```