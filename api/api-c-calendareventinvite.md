# API C Calendar.EventInvite

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Invites a player to the currently selected event.
 C_Calendar.EventInvite(name)

==Arguments==
:;name:{{apitype|string}}

==Details==
* You can't do invites while another calendar action is pending.
* Register to the event "CALENDAR_ACTION_PENDING" and using that, check with {{api|C_Calendar.CanSendInvite}} if you can invite.
* Inviting a player who is already on the invitation list will result in a "<Player> has already been invited." dialog box appearing.

==Patch changes==
* {{Patch 8.0.1|note=Moved to {{api|C_Calendar.EventInvite}}.}}
* {{Patch 3.0.2|note=Added as {{api|CalendarEventInvite}}.}}
```