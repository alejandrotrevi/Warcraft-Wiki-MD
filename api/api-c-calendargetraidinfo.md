# API C Calendar.GetRaidInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 info = C_Calendar.GetRaidInfo(offsetMonths, monthDay, eventIndex)

==Arguments==
:;offsetMonths:{{apitype|number}}
:;monthDay:{{apitype|number}}
:;eventIndex:{{apitype|number}}

==Returns==
:;info:structure - CalendarRaidInfo

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| name || {{apitype|string}} ||
|-
| calendarType || {{apitype|string}} ||
|-
| raidID || {{apitype|number}} ||
|-
| time || structure CalendarTime ||
|-
| difficulty || {{apitype|number}} ||
|-
| difficultyName || {{apitype|string?}} ||
|}</onlyinclude>

{{:Struct_Calendar.CalendarTime}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```