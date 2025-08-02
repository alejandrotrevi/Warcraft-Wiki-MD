# API UnitIsSameServer

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns true if the unit is from the same (connected) realm.
 sameServer = UnitIsSameServer(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;sameServer:{{apitype|boolean}} - 1 if the specified unit is from the player's realm (or a [[Connected Realm]] linked to the player's own realm), nil otherwise.

==Patch changes==
* {{Patch 5.4.0|note=First parameter argument; now always compares the realm of the specified unit to the player's own realm.}}
* {{Patch 4.1.0|note=Added.}}

==See also==
* {{api|UnitRealmRelationship}}
```