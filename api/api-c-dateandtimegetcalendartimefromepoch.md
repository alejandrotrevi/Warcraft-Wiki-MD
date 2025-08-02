# API C DateAndTime.GetCalendarTimeFromEpoch

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_DateAndTime|system=DateAndTime}}
Returns the date for a specified amount of time since the UNIX epoch for the OS time zone.
 date = C_DateAndTime.GetCalendarTimeFromEpoch(epoch)

==Arguments==
:;epoch:{{apitype|number}} - time in microseconds

==Returns==
:;date:{{apitype|CalendarTime}}
{{:Struct Calendar.CalendarTime|nocaption=1}}

==Example==
 local d = C_DateAndTime.GetCalendarTimeFromEpoch(1e6 * 60 * 60 * 24)
 print(format("One day since epoch is %d-%02d-%02d %02d:%02d", d.year, d.month, d.monthDay, d.hour, d.minute))

 > One day since epoch is 1970-01-02 01:00

==Patch changes==
* {{Patch 8.1.0|note=Moved to '''C_DateAndTime.GetCalendarTimeFromEpoch'''(), the previous alias is deprecated. [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#40]}}
* {{Patch 8.0.1|note=Added as '''C_DateAndTime.GetDateFromEpoch'''()}}
```