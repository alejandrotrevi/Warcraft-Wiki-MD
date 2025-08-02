# API GetMirrorTimerInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the mirror timer, e.g. fatigue, breath and feign death.
 timer, initial, maxvalue, scale, paused, label = GetMirrorTimerInfo(id)

==Arguments==
:;id:{{apitype|number}} - timer index, from 1 to MIRRORTIMER_NUMTIMERS (3 as of 3.2). In general, the following correspondence holds: 1 = Fatigue, 2 = Breath, 3 = Feign Death.

==Returns==
:;timer:{{apitype|string}} - A string identifying timer type; "EXHAUSTION", "BREATH", and "FEIGNDEATH", or "UNKNOWN" indicating that the timer corresponding to that index is not currently active, and other return values are invalid.
:;initial:{{apitype|number}} - Value of the timer when the it started.
:;maxvalue:{{apitype|number}} - Maximum value of the timer.
:;scale:{{apitype|number}} - Change in timer value per second.
:;paused:{{apitype|boolean}} - 0 if the timer is currently running, a value greater than zero if it is not.
:;label:{{apitype|string}} - Localized timer name.

==Details==
* Calling the function with an out-of-range index results in an error. The syntax specification in the error text is invalid; this function may not be called with "BREATH", "EXHAUSTION" etc as arguments.
* The current value of the timer may be retrieved using {{api|GetMirrorTimerProgress}}("timer"). Most timers tend to count down to zero, at which point something bad happens.

==Related events==
* {{api|t=e|MIRROR_TIMER_START}} is fired when a timer becomes active.
* {{api|t=e|MIRROR_TIMER_STOP}} is fired when a timer becomes inactive.
* {{api|t=e|MIRROR_TIMER_PAUSE}} is fired when a timer is paused.
```