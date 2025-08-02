# API ConfirmReadyCheck

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Responds to a ready check.
 ConfirmReadyCheck(isReady)

==Arguments==
:;isReady:{{apitype|number?}} - 1 if the player is ready, nil if the player is not ready

==Details==
This function is used in response to receiving a READY_CHECK event. Normally this event will display the ReadyCheckFrame dialog which will in turn call ConfirmReadyCheck in response to the user clicking the Yes or No button.
```