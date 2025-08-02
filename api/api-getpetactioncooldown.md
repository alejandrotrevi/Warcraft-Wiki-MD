# API GetPetActionCooldown

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns cooldown info for an action on the pet action bar.
 startTime, duration, enable = GetPetActionCooldown(index)

==Arguments==
:;index:{{apitype|number}} - The index of the pet action button you want to query for cooldown info.

==Returns==
:;startTime:{{apitype|number}} - The time when the cooldown started (as returned by [[API GetTime|GetTime()]]) or zero if no cooldown
:;duration:{{apitype|number}} - The number of seconds the cooldown will last, or zero if no cooldown
:;enable:{{apitype|number}} - 0 if no cooldown, 1 if cooldown is in effect (probably)
```