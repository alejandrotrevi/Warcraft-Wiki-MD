# API C Garrison.GetFollowerItems

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Return information about a follower weapon and armor.

 weaponItemID, weaponItemLevel, armorItemID, armorItemLevel = C_Garrison.GetFollowerItems(followerID)

==Arguments==
:;followerID:{{apitype|string}} : [[GUID#Follower|FollowerGUID]]

==Returns==
:;weaponItemID:{{apitype|number}} - ItemID for displayed item texture
:;weaponItemLevel:{{apitype|number}} - Current weapon item level
:;armorItemID:{{apitype|number}} - ItemID for displayed item texture
:;armorItemLevel:{{apitype|number}} - Current armor item level

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```