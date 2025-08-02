# API C Calendar.GetClubCalendarEvents

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 events = C_Calendar.GetClubCalendarEvents(clubId, startTime, endTime)

==Arguments==
:;clubId:{{apitype|string}}
:;startTime:{{apitype|CalendarTime}}
:;endTime:{{apitype|CalendarTime}}
{{:Struct CalendarTime|nocaption=1}}

==Returns==
:;events:{{apitype|CalendarDayEvent[]}}
{{:Struct CalendarDayEvent|nocaption=1}}

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```