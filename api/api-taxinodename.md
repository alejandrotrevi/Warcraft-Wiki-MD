# API TaxiNodeName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of a flight path node.
 name = TaxiNodeName(index)

==Arguments==
:;index:{{apitype|number}} - Index of the taxi map node, ascending from 1 to {{api|NumTaxiNodes}}()

==Returns==
:;name:{{apitype|string}} - name of the specified flight point, or "INVALID" if the index is out of bounds.

==Details==
* Taxi information is only available while the taxi map is open -- between the {{api|t=e|TAXIMAP_OPENED}} and {{api|t=e|TAXIMAP_CLOSED}} events.
```