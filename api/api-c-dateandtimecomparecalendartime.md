# API C DateAndTime.CompareCalendarTime

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_DateAndTime|system=DateAndTime}}
Compares two dates with eachother.
 comparison = C_DateAndTime.CompareCalendarTime(lhsCalendarTime, rhsCalendarTime)

==Arguments==
:;lhsCalendarTime:{{apitype|CalendarTime}} - left-hand side time
:;rhsCalendarTime:{{apitype|CalendarTime}} - right-hand side time
{{:Struct Calendar.CalendarTime|nocaption=1}}

==Returns==
:;comparison:{{apitype|number}}
:: <code>1</code> : rhsCalendarTime is at a later time
:: <code>0</code> : rhsCalendarTime is at the same time
:: <code>-1</code> : rhsCalendarTime is at an earlier time

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```