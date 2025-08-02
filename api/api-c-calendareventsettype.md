# API C Calendar.EventSetType

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the event type for the current calendar event.
 C_Calendar.EventSetType(typeIndex)

==Arguments==
:;typeIndex:enum - CalendarEventType
{{:Enum_Calendar.CalendarEventType}}

==Details==
* The calendar event must be previously opened with {{api|C_Calendar.OpenEvent}} or an event candidate from {{api|C_Calendar.CreatePlayerEvent}}.
* The calendar event is updated with {{api|C_Calendar.UpdateEvent}} or created with {{api|C_Calendar.AddEvent}}.
* If the event type is not set before creating with ''C_Calendar.AddEvent'', it defaults to 1.

==Patch changes==
* {{Patch 8.0.1|note=Moved to {{api|C_Calendar.EventSetType}}.}}
* {{Patch 3.0.2|note=Added as {{api|CalendarEventSetType}}.}}
```