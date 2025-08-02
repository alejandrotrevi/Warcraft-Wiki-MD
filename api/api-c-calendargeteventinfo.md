# API C Calendar.GetEventInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Calendar|system=Calendar}}
{{api ambox|This is a stateful API – the current calendar event is set with {{api|C_Calendar.OpenEvent}}.}}
<!--desc-->Returns info for a calendar event.
 info = C_Calendar.GetEventInfo()

==Returns==
:;info:{{apitype|CalendarEventInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| title || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| creator || {{apitype|string?}} || The name of the character who created the event.
|-
| eventType || {{apitype|Enum.CalendarEventType}} || The type of event as specified by {{api|C_Calendar.EventSetType}}.
|-
| repeatOption || {{apitype|Enum.CalendarEventRepeatOptions}} || The repeat setting.
|-
| maxSize || {{apitype|number}} || Usually 100.
|-
| textureIndex || {{apitype|number?}} || The index of the event's texture in the list returned by {{api|C_Calendar.EventGetTextures}}.
|-
| time || {{apitype|CalendarTime}} || When the event occurs.
|-
| lockoutTime || {{apitype|CalendarTime}} || 
|-
| isLocked || {{apitype|boolean}} || Whether the event is locked.
|-
| isAutoApprove || {{apitype|boolean}} || Whether signups to the event should be automatically approved. 
|-
| hasPendingInvite || {{apitype|boolean}} || Whether the player has been invited to this event and has not yet responded.
|-
| inviteStatus || {{apitype|Enum.CalendarStatus?}} || The character's current invite status for the event.
|-
| inviteType || {{apitype|Enum.CalendarInviteType?}} || 
|-
| calendarType || {{apitype|string}} || const CALENDARTYPE
|-
| communityName || {{apitype|string?}} || 
|}

{{:Enum.CalendarEventType}}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.CalendarEventRepeatOptions
! Value !! Field !! Description
|-
| 0 || Never || 
|-
| 1 || Weekly || 
|-
| 2 || Biweekly || 
|-
| 3 || Monthly || 
|}

{{:Struct CalendarTime}}

{{:Enum.CalendarStatus}}

{{:Enum.CalendarInviteType}}

{{:Const_CALENDARTYPE}}
```