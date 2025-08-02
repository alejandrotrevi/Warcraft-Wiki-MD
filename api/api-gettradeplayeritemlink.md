# API GetTradePlayerItemLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item link for an item in the trade window.
 itemLink = GetTradePlayerItemLink(index)

==Arguments==
:;index:{{apitype|number}} - index value of your character's trade slots. Starts at 1 and proceeds to 7 (<code>MAX_TRADE_ITEMS</code>). 7 may be used for the will-not-be-traded-slot.

==Returns==
:;itemLink:{{apitype|string}} : [[ItemLink]] - a string that can be used to link items in the chat log
```