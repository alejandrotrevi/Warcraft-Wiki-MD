# API C DateAndTime.AdjustTimeByDays

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_DateAndTime|system=DateAndTime}}
Returns the date after a specified amount of days.
 newDate = C_DateAndTime.AdjustTimeByDays(date, days)
         = C_DateAndTime.AdjustTimeByMinutes(date, minutes)

==Arguments==
===<font color="#4ec9b0">AdjustTimeByDays</font>===
:;date:{{apitype|CalendarTime}}
:;days:{{apitype|number}}

===<font color="#4ec9b0">AdjustTimeByMinutes</font>===
:;date:{{apitype|CalendarTime}}
:;minutes:{{apitype|number}}

==Returns==
:;newDate:{{apitype|CalendarTime}}
{{:Struct Calendar.CalendarTime|nocaption=1}}

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```