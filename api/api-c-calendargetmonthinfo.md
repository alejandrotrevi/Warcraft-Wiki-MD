# API C Calendar.GetMonthInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the calendar month by offset.
 monthInfo = C_Calendar.GetMonthInfo([offsetMonths])

==Arguments==
:;offsetMonths:{{apitype|number?|default=0}} - Offset in months from the currently selected Calendar month, positive numbers indicating future months.

==Returns==
:;monthInfo:structure - CalendarMonthInfo

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| month || {{apitype|number}} || Month index (1-12)
|-
| year || {{apitype|number}} || Year at the offset date (2004+)
|-
| numDays || {{apitype|number}} || Number of days in the month (28-31)
|-
| firstWeekday || {{apitype|number}} || Weekday on which the month begins (1 = Sunday, 2 = Monday, ..., 7 = Saturday)
|}

==Details==
* This function returns information based on the currently selected calendar month (per {{api|C_Calendar.SetMonth}}). Prior to opening the calendar for the first time in a given session, this is set to {{api|C_Calendar.GetMinDate}} (i.e. November 2004).

==Patch changes==
* {{Patch 8.0.1|note=Moved to {{api|C_Calendar.GetMonthInfo}}.}}
* {{Patch 3.0.2|note=Added as {{api|CalendarGetMonth}}.}}
```