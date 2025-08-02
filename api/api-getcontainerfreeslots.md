# API GetContainerFreeSlots

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__

Populates a table with references to unused slots inside a [[Bag|container]].

 returnTable = GetContainerFreeSlots(index)
 GetContainerFreeSlots(index, returnTable);

==Arguments==
:;index:{{apitype|number}} - the slot containing the bag, e.g. 0 for backpack, etc.
:;returnTable:{{apitype|table?}} - Provide an empty table and the function will populate it with the free slots

==Returns==
:;returnTable:{{apitype|table}} - If you do not specify returnTable as an argument, the function constructs and returns a new table instead

==See also==
* {{api|GetContainerNumFreeSlots}}
```