# API GetInspectPVPRankProgress

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the inspected unit's progress towards the next PvP rank.
 rankProgress = GetInspectPVPRankProgress()

==Returns==
:;rankProgress:{{apitype|number}} - The progress made toward the next PVP rank normalized between 0 and 1

==Details==
* Requires you to be inspecting a unit and call {{api|GetInspectHonorData}}() first before this api returns updated information.
* If not inspecting a unit, {{api|NotifyInspect}}("unit") must be called first.

==Patch changes==
* {{Patch 2.0.1|note=Removed.}}
* {{Patch 1.6.0|note=Added.}}
```