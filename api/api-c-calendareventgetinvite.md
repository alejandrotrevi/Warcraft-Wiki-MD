# API C Calendar.EventGetInvite

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Calendar|system=Calendar}}
Returns status information for an invitee for the currently opened event.
 info = C_Calendar.EventGetInvite(eventIndex)

==Arguments==
:;eventIndex:{{apitype|number}} - Ranging from 1 to {{api|C_Calendar.GetNumInvites}}()

==Returns==
:;info:{{apitype|CalendarEventInviteInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string?}} || 
|-
| level || {{apitype|number}} || 
|-
| className || {{apitype|string?}} || 
|-
| classFilename || {{apitype|string?}} || 
|-
| inviteStatus || {{apitype|Enum.CalendarStatus?}} || 
|-
| modStatus || {{apitype|string?}} || "MODERATOR", "CREATOR"<sup>[https://www.townlong-yak.com/framexml/live/Blizzard_Calendar/Blizzard_Calendar.lua#3370]</sup>
|-
| inviteIsMine || {{apitype|boolean}} || True if the selected entry is the player
|-
| type || {{apitype|Enum.CalendarInviteType}} || 
|-
| notes || {{apitype|string}} || 
|-
| classID || {{apitype|number?}} || 
|-
| guid || {{apitype|string}} || 
|}

{{:Enum.CalendarStatus}}

{{:Enum.CalendarInviteType}}

==Patch changes==
* {{Patch 8.2.5|note=Added <code>classID, guid</code> fields.}}
* {{Patch 8.0.1|note=Moved to <code>C_Calendar.EventGetInvite()</code>}}
* {{Patch 3.0.2|note=Added as <code>CalendarEventGetInvite()</code>}}
```