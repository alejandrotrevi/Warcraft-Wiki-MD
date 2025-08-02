# API C Calendar.GetDayEvent

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieve information about the specified calendar event.
 event = C_Calendar.GetDayEvent(monthOffset, monthDay, index)

==Arguments==
:;monthOffset:{{apitype|number}} - the number of months to offset from today.
:;monthDay:{{apitype|number}} - the desired day of the month the event exists on.
:;index:{{apitype|number}} -  the index of the desired event, from 1 through {{api|C_Calendar.GetNumDayEvents}}.

==Returns==
:;event:{{apitype|CalendarDayEvent}}
{{:Struct CalendarDayEvent|nocaption=1}}

==Details==
: This data seems to be inaccurate until {{api|t=e|PLAYER_ENTERING_WORLD}} fires.

==Patch changes==
* {{Patch 7.2.0|note=Returns structured data and moved to {{api|C_Calendar.GetDayEvent}}()<sup>[https://www.townlong-yak.com/framexml/7.3.5/Blizzard_Deprecated/Deprecated_7_2_0.lua#187]</sup>}}
* {{Patch 3.0.2|note=Added as <code>CalendarGetDayEvent()</code>}}
```