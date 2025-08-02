# API GetInviteConfirmationInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves information about a player that could be invited.
 confirmationType, name, guid, rolesInvalid, willConvertToRaid, level, spec, itemLevel = GetInviteConfirmationInfo(guid)

==Arguments==
:;guid:{{apitype|unknown}} - return value of function {{api|GetNextPendingInviteConfirmation}}

==Returns==
:;confirmationType:{{apitype|number}} - Integer value related to constants like LE_INVITE_CONFIRMATION_REQUEST
:;name:{{apitype|string}} - name of the player
:;guid:{{apitype|string}} - a string containing the hexadecimal representation of the player's [[GUID]]. Player-[server ID]-[player UID] (Example: "Player-976-0002FD64")
:;rolesInvalid:{{apitype|boolean}} - The player has no valid roles.
:;willConvertToRaid:{{apitype|boolean}} - Inviting this player or group will convert your party to a raid.
:;level:{{apitype|number}} - player level
:;spec:{{apitype|number}} - player specialization id. The player specialization name can be requested by {{api|GetSpecializationInfoByID}}.
:;itemLevel:{{apitype|number}} - player item level

==Related Constants==
* LE_INVITE_CONFIRMATION_QUEUE_WARNING = 3 
* LE_INVITE_CONFIRMATION_RELATION_NONE = 0 
* LE_INVITE_CONFIRMATION_RELATION_FRIEND = 1 
* LE_INVITE_CONFIRMATION_RELATION_GUILD = 2
* LE_INVITE_CONFIRMATION_REQUEST = 1
* LE_INVITE_CONFIRMATION_SUGGEST = 2
```