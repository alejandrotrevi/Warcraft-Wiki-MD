# API GetContainerNumFreeSlots

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of free slots in a bag.
 numberOfFreeSlots, bagType = GetContainerNumFreeSlots([[bagID]])

==Arguments==
:;[[bagID]]:{{apitype|number}} - the slot containing the bag, e.g. 0 for backpack, etc.

==Returns==
:;numberOfFreeSlots:{{apitype|number}} - the number of free slots in the specified bag.
:;bagType:{{apitype|number}} ([[itemFamily]] Bitfield) - The type of the container, described using [[itemFamily|bits]] to indicate its permissible contents.

==See also==
*{{api|GetContainerFreeSlots}} - Returns a table containing references to each free slot
```