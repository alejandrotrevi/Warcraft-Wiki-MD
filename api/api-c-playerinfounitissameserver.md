# API C PlayerInfo.UnitIsSameServer

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if a player is from the same or [[Connected Realm|connected]] realm.
 unitIsSameServer = C_PlayerInfo.UnitIsSameServer(playerLocation)

==Arguments==
:;playerLocation:{{apitype|PlayerLocationMixin}}

==Returns==
:;unitIsSameServer:{{apitype|boolean}}

==Example==
Shows if your target is on the same (connected) realm.
 /dump C_PlayerInfo.UnitIsSameServer(PlayerLocation:CreateFromUnit("target"))

==Patch changes==
* {{Patch 8.1.5|note=Added.}}

==See also==
* {{api|UnitIsSameServer}}
```