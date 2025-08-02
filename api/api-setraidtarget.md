# API SetRaidTarget

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Assigns a [[Target marker|raid target]] icon to a unit.
 SetRaidTarget(unit, index)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]
:;index:{{apitype|number}} - Raid target index to assign to the specified unit:
{{:API GetRaidTargetIndex}}

==Details==
* The icons are only visible to your group. In a 5-man party, all party members may assign raid icons. In a raid, only the raid leader and the assistants may do so.
* This API toggles the icon if it's already assigned to the unit.<!-- The {{api|SetRaidTargetIcon}}() 
FrameXML function also provides this toggling behaviour. -->
* Units can only be assigned one icon at a time; and each icon can only be assigned to one unit at a time.
{| {{apitable}}
{{apirow | Related API | {{api|GetRaidTargetIndex}} }}
{{apirow | Related Events | {{api|t=e|RAID_TARGET_UPDATE}} }}
{{apirow | Related FrameXML | [https://www.townlong-yak.com/framexml/live/go/SetRaidTargetIcon SetRaidTargetIcon] }}
|}

==Example==
To set a skull over your current target:
<syntaxhighlight lang="lua">
/run SetRaidTarget("target", 8)
</syntaxhighlight>

Without toggling behavior:
<syntaxhighlight lang="lua">
/run if GetRaidTargetIndex("target") ~= 8 then SetRaidTarget("target", 8) end
</syntaxhighlight>

==Patch changes==
* {{Patch 9.2.0|note=Removed invisible IDs 9 to 18.}}
* {{Patch 1.11.0|note=Added.}}

==See also==
* [[RaidFlag]]
```