# API C Calendar.GetHolidayInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Calendar|system=Calendar}}
Returns seasonal holiday info.
 event = C_Calendar.GetHolidayInfo(monthOffset, monthDay, index)

==Arguments==
:;monthOffset:{{apitype|number }} - The offset from the current month (only accepts 0 or 1).
:;monthDay:{{apitype|number}} - The day of the month.
:;index:{{apitype|number}}

==Returns==
:;event:{{apitype|CalendarHolidayInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| texture || {{apitype|number}} || 
|-
| startTime || {{apitype|CalendarTime?}} || 
|-
| endTime || {{apitype|CalendarTime?}} || 
|}

{{:Struct CalendarTime}}

==Patch changes==
* {{Patch 7.2.0|note=Returns structured data and moved to <code>C_Calendar.GetHolidayInfo()</code><sup>[https://www.townlong-yak.com/framexml/7.3.5/Blizzard_Deprecated/Deprecated_7_2_0.lua#205]</sup>}}
* {{Patch 3.1.3|note=Added as <code>CalendarGetHolidayInfo()</code>}}
```