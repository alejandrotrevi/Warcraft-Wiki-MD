# API C AuctionHouse.MakeItemKey

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns an auction house item key.
 itemKey = C_AuctionHouse.MakeItemKey(itemID [, itemLevel [, itemSuffix [, battlePetSpeciesID]]])

==Arguments==
:;itemID:{{apitype|number}}
:;itemLevel:{{apitype|number?|default=0}}
:;itemSuffix:{{apitype|number?|default=0}}
:;battlePetSpeciesID:{{apitype|number?|default=0}} : [[BattlePetSpeciesID]]

==Returns==
:;itemKey:{{apitype|ItemKey}}
{{:Struct AuctionHouse.ItemKey|nocaption=1}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```