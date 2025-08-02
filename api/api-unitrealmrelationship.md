# API UnitRealmRelationship

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns information about the player's relation to the specified unit's realm.
 realmRelationship = UnitRealmRelationship(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;realmRelationship:{{apitype|number}} - if the specified unit is a player, one of:
:* <code>LE_REALM_RELATION_SAME</code> = 1 - unit and player are from the same realm.
:* <code>LE_REALM_RELATION_COALESCED</code> = 2 - unit and player are coalesced from unconnected realms.
:* <code>LE_REALM_RELATION_VIRTUAL</code> = 3 - unit and player are from [[Connected Realm]]s.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}

==See also==
* {{api|UnitName}}
```