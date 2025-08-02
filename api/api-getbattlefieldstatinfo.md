# API GetBattlefieldStatInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Get list of battleground specific columns on the scoreboard.
 name, icon, tooltip = GetBattlefieldStatInfo(index)

===Arguments===
:;index:{{apitype|number}} - Column to get data for

==Returns==
:;name:{{apitype|string}} - Name of the column (eg: Flags Captured)
:;icon:{{apitype|string}} - Icon displayed when on the scoreboard rows (eg: Horde flag icon next to the flag captures of an [[Alliance]] player)
:;tooltip:{{apitype|string}} - Tooltip displayed when hovering over a column's name

==Details==
Used to retrieve the custom scoreboard columns inside a battleground.

====Warsong Gulch====
*Flags Captured
*Flags Returned

====Arathi Basin====
*Bases Assaulted
*Bases Defended

====Alterac Valley====
*Graveyards Assaulted
*Graveyards Defended
*Towers Assaulted
*Towers Defended
*Mines Captured
*Leaders Killed
*Secondary Objectives

==Patch changes==
* {{Patch 8.2.0|note=Deprecated.[https://www.townlong-yak.com/framexml/8.2.0/Blizzard_Deprecated/Deprecated_8_2_0.lua#21]}}
```