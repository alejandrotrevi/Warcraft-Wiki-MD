# API SetAutoDeclineGuildInvites

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Sets whether guild invites should be automatically declined.
 SetAutoDeclineGuildInvites(decline)

==Arguments==
:;decline:{{apitype|boolean}} - True if guild invitations should be automatically declined, false if invitations should be shown to the user.

==Triggers events==
* {{api|t=e|DISABLE_DECLINE_GUILD_INVITE}}, if guild invitations will now be shown to the user
* {{api|t=e|ENABLE_DECLINE_GUILD_INVITE}}, if guild invitations will now be declined automatically

==Details==
Blizzard's code always passes in a string value, but the function accepts both strings and numbers, just like {{api|SetCVar}}, and its counterpart {{api|GetAutoDeclineGuildInvites}} returns numeric values, just like {{api|GetCVar}}.

==See also==
* {{api|GetAutoDeclineGuildInvites}}
```