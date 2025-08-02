# API C BlackMarket.Close

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Closes the [[Black Market]] window.
 C_BlackMarket.Close()

==Triggers events==
* {{api|t=e|BLACK_MARKET_CLOSE}}

==Details==
* While the black market UI is considered open, the server may notify the client about black market auction updates.
* This function is called by FrameXML when the player manually closes the Black Market window.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```