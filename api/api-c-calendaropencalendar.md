# API C Calendar.OpenCalendar

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Requests calendar information from the server. Does not open the calendar frame.
 C_Calendar.OpenCalendar()

==Details==
* Fires {{api|t=e|CALENDAR_UPDATE_EVENT_LIST}}, when your query has finished processing on the server and new calendar information is available.
* If called during the loading process, (even at {{api|t=e|PLAYER_ENTERING_WORLD}}) the query will not return.

==Patch changes==
* {{Patch 8.0.1|note=Moved to {{api|C_Calendar.OpenCalendar}}.}}
* {{Patch 3.0.2|note=Added as {{api|OpenCalendar}}.}}
```