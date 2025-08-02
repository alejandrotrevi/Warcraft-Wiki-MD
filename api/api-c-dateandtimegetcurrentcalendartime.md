# API C DateAndTime.GetCurrentCalendarTime

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_DateAndTime|system=DateAndTime}}
Returns the realm's current date and time.
 currentCalendarTime = C_DateAndTime.GetCurrentCalendarTime()

==Returns==
:;currentCalendarTime:{{apitype|CalendarTime}}
{{:Struct Calendar.CalendarTime|nocaption=1}}

==Example==
<syntaxhighlight lang="lua">
local d = C_DateAndTime.GetCurrentCalendarTime()
local weekDay = CALENDAR_WEEKDAY_NAMES[d.weekday]
local month = CALENDAR_FULLDATE_MONTH_NAMES[d.month]
print(format("The time is %02d:%02d, %s, %d %s %d", d.hour, d.minute, weekDay, d.monthDay, month, d.year))
-- The time is 07:55, Friday, 15 March 2019
</syntaxhighlight>

==Comparison==
{{:API_GetServerTime}}

==Patch changes==
* {{Patch 8.1.0|note=Moved to <code>C_DateAndTime.GetCurrentCalendarTime()</code>. The previous alias is deprecated [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#27]. See [https://github.com/Gethe/wow-ui-source/blob/8.3.7/AddOns/Blizzard_Deprecated/Deprecated_8_1_0.lua#L30 ConvertToOldStyleDate()] for changes with the old format.}}
* {{Patch 8.0.1|note=Moved to <code>C_Calendar.GetDate()</code>}}
* {{Patch 3.0.2|note=Added as <code>CalendarGetDate()</code>}}
```