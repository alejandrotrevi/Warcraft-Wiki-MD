# API C Calendar.GetNumDayEvents

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of events for a given day/month offset.
 numDayEvents = C_Calendar.GetNumDayEvents(offsetMonths, monthDay)

==Arguments==
:;offsetMonths:{{apitype|number}} - The number of months to advance from today.
:;monthDay:{{apitype|number}} - The day of the given month.

==Returns==
:;numDayEvents:{{apitype|number}} - The number of events on the day in question.

==Patch changes==
* {{Patch 8.0.1|note=Moved to {{api|C_Calendar.GetNumDayEvents}}.}}
* {{Patch 3.0.2|note=Added as {{api|CalendarGetNumDayEvents}}.}}
```