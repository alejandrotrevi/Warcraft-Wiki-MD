# API GetVoidItemHyperlinkString

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item link of an item in void storage.
 itemLink = GetVoidItemHyperlinkString(voidSlot)

==Arguments==
:;voidSlot:{{apitype|number}} - index of the void storage slot to query, ascending from 1.
:: <b>Note:</b> The index starts from top to bottom first (vertically), then left to right (horizontally), and then continues the same process with the next tab.

==Returns==
:;itemLink:{{apitype|string}} - [[item link]] of the item in the queried void storage slot; nil if the slot is empty.

==Patch changes==
* {{Patch 4.3.0|note=Added.}}

==See also==
* {{api|t=w|GetVoidItemInfo}}
```