# API GetRaidTargetIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the [[Target marker|raid target]] of a unit.
 index = GetRaidTargetIndex(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;index:{{apitype|number?}}
<onlyinclude>{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Icon
|-
| 1 || {{Raidicon|Star}} Yellow 4-point Star
|-
| 2 || {{Raidicon|Circle}} Orange Circle
|-
| 3 || {{Raidicon|Diamond}} Purple Diamond
|-
| 4 || {{Raidicon|Triangle}} Green Triangle
|-
| 5 || {{Raidicon|Moon}} White Crescent Moon
|-
| 6 || {{Raidicon|Square}} Blue Square
|-
| 7 || {{Raidicon|Cross}} Red "X" Cross
|-
| 8 || {{Raidicon|Skull}} White Skull
|}</onlyinclude>

==Details==
* Raid target icons are typically displayed by unit frames, as well as above the marked entities in the 3D world. The targets can be assigned by raid leaders and assistants, party members, and the player while soloing, and are only visible to other players within the same group.
* This function can return arbitrary values if the queried unit does not exist. Use {{api|UnitExists}}() to check whether a unit is valid.
*: For example: "raid2target" when "raid2" is offline and not targetting anything at all misbehaves.
{| {{apitable}}
{{apirow | Related API | {{api|SetRaidTarget}} }}
{{apirow | Related Events | {{api|t=e|RAID_TARGET_UPDATE}} }}
|}

==Example==
Prints the raid target index for your target.
 /dump GetRaidTargetIndex("target")

==Patch changes==
* {{Patch 9.2.0|note=Removed invisible IDs 9 to 18.}}
* {{Patch 1.11.0|note=Added.}}

==See also==
* [[RaidFlag]]
```