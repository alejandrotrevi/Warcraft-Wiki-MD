# API CollapseFactionHeader

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Collapse a faction header row.
 CollapseFactionHeader(rowIndex)

==Arguments==
:;rowIndex:{{apitype|number}} - The row index of the header to collapse (Specifying a non-header row can have unpredictable results). The UPDATE_FACTION event is fired after the change since faction indexes will have been shifted around.

==See also==
[[API_ExpandFactionHeader|ExpandFactionHeader]]
```