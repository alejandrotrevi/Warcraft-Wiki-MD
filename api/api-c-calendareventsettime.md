# API C Calendar.EventSetTime

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the time for the currently opened event.
 C_Calendar.EventSetTime(hour, minute)

==Arguments==
:;hour:{{apitype|number}}
:;minute:{{apitype|number}}

==Details==
* The calendar event must be previously opened with {{api|C_Calendar.OpenEvent}} or an event candidate from {{api|C_Calendar.CreatePlayerEvent}} and similar.
* The calendar event is updated with {{api|C_Calendar.UpdateEvent}} or created with {{api|C_Calendar.AddEvent}}.

==Patch changes==
* {{Patch 8.0.1|note=Moved to {{api|C_Calendar.EventSetTime}}.}}
* {{Patch 3.0.2|note=Added as {{api|CalendarEventSetTime}}.}}
```