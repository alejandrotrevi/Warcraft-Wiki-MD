# API C AuctionHouse.IsSellItemValid

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns true if an item from your bag can be posted on the auction house.
 valid = C_AuctionHouse.IsSellItemValid(item [, displayError])

==Arguments==
:;item:{{apitype|ItemLocationMixin}}
:;displayError:{{apitype|boolean?|default=true}}

==Returns==
:;valid:{{apitype|boolean}}

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```