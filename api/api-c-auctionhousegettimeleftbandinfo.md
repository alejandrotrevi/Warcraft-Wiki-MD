# API C AuctionHouse.GetTimeLeftBandInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Identifies the breakpoints for describing an auction's remaining duration using time-left bands.
 timeLeftMinSeconds, timeLeftMaxSeconds = C_AuctionHouse.GetTimeLeftBandInfo(timeLeftBand)

==Arguments==
:;timeLeftBand:{{apitype|Enum.AuctionHouseTimeLeftBand}}
{{:Enum AuctionHouse.AuctionHouseTimeLeftBand|nocaption=1}}

==Returns==
:;timeLeftMinSeconds:{{apitype|number}} - Minimum duration for auctions in this band.
:;timeLeftMaxSeconds:{{apitype|number}} - Maximum duration for auctions in this band.

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```