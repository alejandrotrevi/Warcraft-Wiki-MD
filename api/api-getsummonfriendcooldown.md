# API GetSummonFriendCooldown

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6}}
Returns the cooldown info of the RaF Summon Friend ability.
 start, duration = GetSummonFriendCooldown()

==Returns==
:;start:{{apitype|number}} - The value of {{api|GetTime}}() at the moment the cooldown began, 0 if the ability is ready
:;duration:{{apitype|number}} - The length of the cooldown in seconds, 0 if the ability is ready

==Example==
The snippet below prints the remaining time of the cooldown in seconds.
 local start, duration = GetSummonFriendCooldown()
 local timeleft = start + duration - GetTime()
 print(timeleft)
```