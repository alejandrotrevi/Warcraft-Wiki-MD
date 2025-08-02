# API C Calendar.GetGuildEventInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Calendar|system=Calendar}}
Needs summary.
 info = C_Calendar.GetGuildEventInfo(index)

==Arguments==
:;index:{{apitype|number}}

==Returns==
:;info:{{apitype|CalendarGuildEventInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| eventID || {{apitype|string}} || 
|-
| year || {{apitype|number}} || 
|-
| month || {{apitype|number}} || 
|-
| monthDay || {{apitype|number}} || 
|-
| weekday || {{apitype|number}} || 
|-
| hour || {{apitype|number}} || 
|-
| minute || {{apitype|number}} || 
|-
| eventType || {{apitype|Enum.CalendarEventType}} || 
|-
| title || {{apitype|string}} || 
|-
| calendarType || {{apitype|string}} || 
|-
| texture || {{apitype|number}} || 
|-
| inviteStatus || {{apitype|number}} || 
|-
| clubID || {{apitype|string}} || 
|}

{{:Enum.CalendarEventType}}

==Patch changes==
* {{Patch 8.1.5|note=Added <code>eventID, year, inviteStatus, clubID</code> fields.}}
* {{Patch 8.0.1|note=Added. See also {{api|GetGuildEventInfo}}()}}
```