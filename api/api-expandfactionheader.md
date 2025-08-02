# API ExpandFactionHeader

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Expand a faction header row.
 ExpandFactionHeader(rowIndex)
==Arguments==
:;rowIndex:{{apitype|number}} - The row index of the header to expand (Specifying a non-header row can have unpredictable results). The UPDATE_FACTION event is fired after the change since faction indexes will have been shifted around.

==See Also==
[[API_CollapseFactionHeader|CollapseFactionHeader]]
```