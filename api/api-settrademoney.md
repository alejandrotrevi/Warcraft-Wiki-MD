# API SetTradeMoney

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the amount of money offered as part of the player's trade offer.
 SetTradeMoney(copper)

==Arguments==
:;copper:{{apitype|number}} - Amount of money, in copper, to offer for trade.

==Example==
The following will put {{cost|g=1}} into the trade window:
 SetTradeMoney(1 * 100 * 100);

==See also==
* {{api|PickupTradeMoney}}
* {{api|AddTradeMoney}}
```