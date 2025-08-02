# API SetPVPRoles

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets which roles the player is willing to perform in PvP battlegrounds.
 SetPVPRoles(tank, healer, dps)

==Arguments==
:;tank:{{apitype|boolean}} - true if the player is willing to tank, false otherwise.
:;healer:{{apitype|boolean}} - true if the player is willing to heal, false otherwise.
:;dps:{{apitype|boolean}} - true if the player is willing to deal damage, false otherwise.

==Triggers events==
* {{api|t=e|PVP_ROLE_UPDATE}}

==Patch changes==
* {{Patch 5.3.0|note=Added.}}

==See also==
* {{api|GetPVPRoles}}
```