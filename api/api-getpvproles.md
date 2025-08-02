# API GetPVPRoles

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns which roles the player is willing to perform in PvP battlegrounds.
 tank, healer, dps = GetPVPRoles()

==Returns==
:;tank:{{apitype|boolean}} - true if the player is marked as willing to tank, false otherwise.
:;healer:{{apitype|boolean}} - true if the player is marked as willing to heal, false otherwise.
:;dps:{{apitype|boolean}} - true if the player is marked as willing to deal damage, false otherwise.

==Patch changes==
* {{Patch 5.3.0|note=Added.}}

==See also==
* {{api|SetPVPRoles}}
* {{api|t=e|PVP_ROLE_UPDATE}}
```