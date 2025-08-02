# API GetFirstBagBankSlotIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index of the first bag slot within the bank container.
 index = GetFirstBagBankSlotIndex()

==Returns==
:;index:{{apitype|number}} - The [[InventorySlotId|slot index]] of the first bank bag.

==Details==

* This function was added to resolve an inconsistency with the value of the <code>NUM_BANKGENERIC_SLOTS</code> constant and the actual slot index assigned to the first bank bag<ref>https://github.com/Stanzilla/WoWUIBugs/issues/187</ref>. On Classic Era, this constant is defined as <code>24</code> matching the number of displayed item slots in the bank frame, however bag slots start at index <code>28</code> as they do on Burning Crusade Classic.

==Patch changes==
===Classic Era===
* {{Patch 1.14.0|note=Added in build 40618 on October 13 2021.}}

==References==
```