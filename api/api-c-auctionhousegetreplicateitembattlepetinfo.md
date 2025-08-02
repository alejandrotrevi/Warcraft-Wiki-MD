# API C AuctionHouse.GetReplicateItemBattlePetInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns display info for a battle pet from a [[API C_AuctionHouse.ReplicateItems|ReplicateItems]] result.
 creatureID, displayID = C_AuctionHouse.GetReplicateItemBattlePetInfo(index)

==Arguments==
:;index:{{apitype|number}}

==Returns==
:;creatureID:{{apitype|number}}
:;displayID:{{apitype|number}}

==Patch changes==
* {{Patch 8.3.0|note=Added. Replaces {{api|GetAuctionItemBattlePetInfo}}(). [https://www.townlong-yak.com/framexml/8.3.0/Blizzard_Deprecated/Deprecated_8_3_0.lua#17]}}

{{apinavbox|C_AuctionHouse}}
```