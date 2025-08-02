# API C Calendar.AddEvent

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent,nofreetrial}}
Saves the new event currently being created to the server.
 C_Calendar.AddEvent()

==Details==
* Finalizes the event candidate created by {{api|C_Calendar.CreatePlayerEvent}}, {{api|C_Calendar.CreateGuildSignUpEvent}} and similar.
* Requires at least {{api|C_Calendar.EventSetTitle}}, {{api|C_Calendar.EventSetDate}} and{{api| C_Calendar.EventSetTime}} to be set.
* This function is only used to create '''new''' events. To save changes to existing events, use {{api|C_Calendar.UpdateEvent}}.

==Example==
Creates an event for tomorrow.

<syntaxhighlight lang="lua">
C_Calendar.CreatePlayerEvent()

local d = C_DateAndTime.GetCurrentCalendarTime()
C_Calendar.EventSetDate(d.month, d.monthDay+1, d.year)
C_Calendar.EventSetTime(d.hour, d.minute)
C_Calendar.EventSetTitle("hello")

C_Calendar.AddEvent()
</syntaxhighlight>

==Patch changes==
* {{Patch 8.0.1|note=Moved to {{api|C_Calendar.AddEvent}}.}}
* {{Patch 3.0.2|note=Added as {{api|CalendarAddEvent}}.}}
```