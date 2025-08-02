# API C LFGList.GetPlaystyleString

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LFGList|system=LFGList}} {{restrictedapi|hwevent}}
Needs summary.
 playstyleString = C_LFGList.GetPlaystyleString(playstyle, activityInfo)

==Arguments==
:;playstyle:{{apitype|Enum.LFGEntryPlaystyle}}
{{:Enum.LFGEntryPlaystyle|nocaption=1}}
:;activityInfo:{{apitype|GroupFinderActivityInfo}}
{{:Struct GroupFinderActivityInfo|nocaption=1}}

==Returns==
:;playstyleString:{{apitype|string}}

==GlobalStrings==
<syntaxhighlight lang="lua">
GROUP_FINDER_PVE_MYTHICZERO_PLAYSTYLE1 = "Standard";
GROUP_FINDER_PVE_MYTHICZERO_PLAYSTYLE2 = "Learning/Progression";
GROUP_FINDER_PVE_MYTHICZERO_PLAYSTYLE3 = "Quick Clear";
GROUP_FINDER_PVE_PLAYSTYLE1 = "Standard";
GROUP_FINDER_PVE_PLAYSTYLE2 = "Completion";
GROUP_FINDER_PVE_PLAYSTYLE3 = "Beat Timer";
GROUP_FINDER_PVE_RAID_PLAYSTYLE1 = "Standard";
GROUP_FINDER_PVE_RAID_PLAYSTYLE2 = "Learning/Progression";
GROUP_FINDER_PVE_RAID_PLAYSTYLE3 = "Quick Clear";
GROUP_FINDER_PVP_PLAYSTYLE1 = "Earn Conquest";
GROUP_FINDER_PVP_PLAYSTYLE2 = "Learning";
GROUP_FINDER_PVP_PLAYSTYLE3 = "Increase Rating";
</syntaxhighlight>

==Patch changes==
* {{Patch 9.1.5|note=Added.}}
```