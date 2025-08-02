# API GetInspectHonorData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns honor info for the inspected player unit.
 todayHK, todayHonor, yesterdayHK, yesterdayHonor, lifetimeHK, lifetimeRank = GetInspectHonorData()

==Returns==
:;todayHK:{{apitype|number}} - Honor kills made today.
:;todayHonor:{{apitype|number}} - Honor rewarded today.
:;yesterdayHK:{{apitype|number}} - Amount of honor kills made yesterday.
:;yesterdayHonor:{{apitype|number}} - The honor rewarded yesterday.
:;lifetimeHK:{{apitype|number}} - Total lifetime honor kills.
:;lifetimeRank:{{apitype|number}} - Highest PvP rank ever attained.

==Details==
* Before this function can return any information, {{api|NotifyInspect}}(unit) must be called first, followed by a call to the {{api|RequestInspectHonorData}} function.
```