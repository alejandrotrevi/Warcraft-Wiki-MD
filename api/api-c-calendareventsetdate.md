# API C Calendar.EventSetDate

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the date for the currently opened event.
 C_Calendar.EventSetDate(month, monthDay, year)

==Arguments==
:;month:{{apitype|number}} - 2 digits [1-12].
:;monthDay:{{apitype|number}} - 2 digits [1-31].
:;year:{{apitype|number}} - 4 digits (2019).

==Details==
* The calendar event must be previously opened with {{api|C_Calendar.OpenEvent}} or an event candidate from {{api|C_Calendar.CreatePlayerEvent}} and similar.
* The calendar event is updated with {{api|C_Calendar.UpdateEvent}} or created with {{api|C_Calendar.AddEvent}}.

==Patch changes==
* {{Patch 8.0.1|note=Moved to {{api|C_Calendar.EventSetDate}}.}}
* {{Patch 3.0.2|note=Added as {{api|CalendarEventSetDate}}.}}
```